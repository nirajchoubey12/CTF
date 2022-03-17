# Hacker Writer

When visiting the url https://hackerwriter.ctf.intigriti.io we don't get anything just a plain screen

![image](https://user-images.githubusercontent.com/19681324/158516882-8796f8ee-0f4c-401a-a5a1-f280898f33a4.png)

Let's check the source of the page
![image](https://user-images.githubusercontent.com/19681324/158516947-d2a46459-e841-4375-bdb7-d2816422af0c.png)

bundle.js file is in the minified format 
![image](https://user-images.githubusercontent.com/19681324/158517021-db06c31e-03f1-4efe-a1b3-bc3f7b9983ed.png)

Use the chrome source tab to format the js in a readable format

![image](https://user-images.githubusercontent.com/19681324/158517559-2fbebe06-a5b0-4edf-bc3e-085572e06080.png)

Formatted bundle.js gives up a new get parameter 
![image](https://user-images.githubusercontent.com/19681324/158517647-d24d94f5-48b6-424d-96a5-cabac79ae405.png)

Going to the url https://hackerwriter.ctf.intigriti.io/?w00t=r00t 
![image](https://user-images.githubusercontent.com/19681324/158517932-c85d6b22-d86e-445e-96a5-0b6bd7c359c4.png)

App was responding with Fuzzing is the key no matter what i did. 
![image](https://user-images.githubusercontent.com/19681324/158732646-bf227ba2-a71a-4c96-b547-fa934af7b788.png)

Then i saw the app backend is php. One of the common way to generate error in php is send the get param as an array. so sent the payload as w00t[]=r00t 
![image](https://user-images.githubusercontent.com/19681324/158732766-4891f548-4aba-4dba-acab-fb577393b33e.png)

Got a different response this time which says the longer the better, lets increase the number of characters in param value
![image](https://user-images.githubusercontent.com/19681324/158732950-5493e697-d9b2-432a-b726-231fd178d58b.png)

Again we get a different response but this time it says script xss me 
![image](https://user-images.githubusercontent.com/19681324/158733238-a7575a3d-0a9d-4080-8aa9-a14ebf900ebf.png)

Now when we try this payload https://hackerwriter.ctf.intigriti.io/?w00t[]=r00tr00tr00tr00tr00tr00tr00tr00tr00tr00tr00tr00tr00tr00tr00tr00t%3Cscript%3Ealert(1)%3C/script%3E  , alert gets executed and we get the flag

![image](https://user-images.githubusercontent.com/19681324/158733333-f1fa3c44-5b89-45af-9813-cc4c489983a8.png)

Other xss payload were not working, so challenge was specifically asking for <script>alert(1)</script> vanilla payload


