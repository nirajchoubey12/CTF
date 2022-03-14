This web challenge is a simple command injection. We just need to find out the exact place of injection with some enumeration

![image](https://user-images.githubusercontent.com/19681324/158090462-92e01970-211d-4d45-b456-1f96d0f99a95.png)

After some browsing through the site we land up on the https://traveller.ctf.intigriti.io/packages.html > https://traveller.ctf.intigriti.io/package2-details.php page

![image](https://user-images.githubusercontent.com/19681324/158090735-b7847d60-b472-4a86-97f5-fad72cb277e3.png)

Here there was an option to submit a form to a php endpoint with few parameteres. When we click on submit after selecting a package below request is sent

![image](https://user-images.githubusercontent.com/19681324/158090924-1b5b6bf4-4cd7-4467-a95e-86002b7ab4c8.png)

But when is tamper with the pack parameter we get the error revealing that it is actually executing a bash command to get the output

![image](https://user-images.githubusercontent.com/19681324/158091012-39b01015-a57a-454b-bbeb-5e730b5e1698.png)

Lets execute the command **& ls /** we get the flag.txt file there. (Here as well you need to enumerate to find exact location of the flag.txt file, root location is an obvious look)

![image](https://user-images.githubusercontent.com/19681324/158091195-af3d105f-2db1-476f-a3e8-8f26a5eaa142.png)

After that we can read the flag

![image](https://user-images.githubusercontent.com/19681324/158091283-a1997509-1000-48cb-8de3-558b7d9c68b1.png)

**Note: Initally i tried ";" as command seperator but didn't get any output after that "&" worked. Find out why ";" didn't work here.**

