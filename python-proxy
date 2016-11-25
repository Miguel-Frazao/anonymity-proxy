import requests, socks, socket

req = requests.get('http://ipinfo.io')
print('Real IP:\n{}'.format(req.json()))

socks.set_default_proxy(socks.SOCKS5, "127.0.0.1", 9050)
socket.socket = socks.socksocket

# HERE FROM NOW WE ARE BEHIND A PROXY

req = requests.get('http://ipinfo.io')
print('\nFake IP:\n{}'.format(req.json()))
