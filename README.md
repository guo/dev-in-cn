# How to dev in China

Due to the well known issue, it is diffcult for developers to do their work in China. A lot of services, repos are not easily accessible in China. This repo contains many tricks and tips to continue your developement work in China. 

## VPN option
It is rather difficult to use VPN now in China. Also some VPN providers do have some options to bypass. Their services are not fully stable. 

## Web access using ShadowSocks
A great project called Showsocks (https://shadowsocks.org/) can help you proxy your traffic to a low-end server from outside China. You can easily create a proxy server yourself by using tools provided on its website: https://shadowsocks.org/en/download/servers.html
I would recommend using an AWS server in JP to host your traffic. 
On your local machine, you can use https://github.com/shadowsocks/ShadowsocksX-NG/releases to config your proxy. By default, you can use "Global mode" to proxy all your traffic. Configuration is also easy. Add a server in servers-> Server Preferences.
You should be able to visit all website using your browser.

## Shell access
You can use `https_proxy` and `http_proxy` in your shell by `export them`:
```
export https_proxy='http://127.0.0.1:1087'
export http_proxy='http://127.0.0.1:1087'
```
You can add it to a bash file to easily enable it.  I personally add it to a bash file named `ss.sh` with content
```
export https_proxy='http://127.0.0.1:1087'
export http_proxy='http://127.0.0.1:1087'
echo 'proxy enabled!'
```

## Telegram 
There is proxy setting in it setting. You can add a SOCK5 proxy pointing to `127.0.0.1:1086` the default port for shadowsocks.

Enjoy your dev in China. 
