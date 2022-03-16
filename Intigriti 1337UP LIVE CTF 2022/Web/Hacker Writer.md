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

