
<div dir="rtl">

[**![persian_lang](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%DA%86%DA%AF%D9%88%D9%86%DA%AF%DB%8C-%DB%8C%D8%A7%D9%81%D8%AA%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%D8%AA%D9%85%DB%8C%D8%B2-%DA%A9%D9%84%D8%A7%D8%AF%D9%81%D9%84%D8%B1)
</div>

# Guide for finding a clean Cloudflare IP
The largest CDN service provider in the world is Cloudflare, and you probably know; Due to the severe filtering of the Internet in Iran, there is a lot of disruption to its services because it is not possible for the filter to completely filter it, but it can cause disruption.
Here, if you also use CDN Cloudflare services; You will be affected by these disorders. To reduce the impact of these disturbances, you should find clean IPs (IPs that are not disturbed).

Here are some ways of working for this issue. 

Tip:
> Before starting, it is emphasized that all these tests must be done on the client system without connecting to VPN.

**Tables of contents:**
- [Using Bashsiz scanner](#using-bashsizs-scanner)
- [Using Farid scanner](#using-vahid-farids-scanner)
- [Using Safarian scanner](#using-safa-safarians-scanner)
- [What to do after finding a clean IP](#what-to-do-after-finding-a-clean-ip)
<br>
<br>

***
<br>
<br>

## Using Bashsiz's scanner
Mr. Bashsiz is an Iranian engineer who has developed a program called CFScanner, which can be used to test the list of Cloudflare IPs on different networks and reach the clean Cloudflare IPs.

This program has been released in several versions including Linux and Windows. Versions available until the date of editing this article:
- Bash
- Docker
- Windows
- Python
- Golang
- Android

To do this, first download the desired version [here](https://github.com/MortezaBashsiz/CFScanner) and then follow how to run it based on the desired operating system.


<details><summary><h3>Run on Linux version</h3> (Click here)</summary>

Download the program files and first see Mr. Bashsiz's explanation of how to run it in the video below (persian).

[![](https://user-images.githubusercontent.com/125398461/229997889-eaf51d2c-e5e1-4899-aa34-6c2c73375f10.png)](https://www.youtube.com/watch?v=BKLRAHolhvM)

This program has prerequisites that must be installed in advance.
[jq](https://stedolan.github.io/jq/)&nbsp;&nbsp;&nbsp;[git](https://git-scm.com/)&nbsp;&nbsp;&nbsp;[tput](https://command-not-found.com/tput)&nbsp;&nbsp;&nbsp;[bc](https://www.gnu.org/software/bc/)&nbsp;&nbsp;&nbsp;[curl](https://curl.se/download.html)&nbsp;&nbsp;&nbsp;
[parallel](https://www.gnu.org/software/parallel/)


Then first clone it on your system with the following code.
```
git clone https://github.com/MortezaBashsiz/CFScanner.git 
```
Go to the app download folder and run access to it. 
```
cd CFScanner/bash
chmod +x ../bin/*
```
Download the config.real file. 
```
curl -s https://raw.githubusercontent.com/MortezaBashsiz/CFScanner/main/bash/ClientConfig.json -o config.real
```
It is recommended to change the config.real file based on your configuration.
 
![PICTURE](https://user-images.githubusercontent.com/125398461/234565256-4ebeb511-4876-483a-84c5-cb39d62a12ae.png)


If you want to have your own configuration file, save it under a different name that will not change when the script is updated.

#### Run the script
Go to the location of the downloaded script file and then run the script as shown below.

```
bash cfScanner.sh SUBNET DOWN threads tryCount config.real speed custom.subnets
```

![222946688-bcec3d65-7bf1-495a-b1bf-fe517f69f8822](https://user-images.githubusercontent.com/125398461/234751332-e0fa6e6b-5b97-445b-bd50-12c9d603d556.png)


For example:


```
bash cfScanner.sh SUBNET DOWN 8 1 config.real 100 custom.subnets
```
Finally, the test result is placed in the `result` folder, which you can view and use. More information on the program [wiki](https://github.com/MortezaBashsiz/CFScanner/tree/main/bash).

</details>

<details><summary><h3>Run on Windows version</h3> (Click here)</summary>

<details><summary><h4>Prerequisites</h4></summary>
First, there must be prerequisites that will be explained in order:

- Download the Windows scanner app from [the project's GitHub](https://github.com/MortezaBashsiz/CFScanner/tree/main/windows)
- Install .NET Desktop Runtime 6 app from the main application site given below

```
https://dotnet.microsoft.com/en-us/download/dotnet/6.0
```

- Checking TLS Handshake
For this, you must first enter the program folder and open `Command Prompt` inside that folder. That is, `Shift+Right click` on the folder and select `Open in Windows Terminal`.

Run the following command in the terminal environment.

`‍‍.\v2ray.exe tls ping sub.yourdomain.com`

Put your subdomain instead of `sub.yourdomain.com`. If handshake `succeeded` message appears; It means that the scanner is ready to use, otherwise you should make temporary changes in the certificate settings on Cloudflare website.

Set the TLS version to TLS 1.0 and disable the TLS 1.3 option.

![Image](https://user-images.githubusercontent.com/125398461/234774581-c1a07bdb-352f-43cc-97f7-2ce6c87a761d.png)

* Note: Don't forget to return these options to the first state after testing.
* Prepare the config template structures for testing.
If you want to test your configurations, you must apply them in the Json file related to the connection in the program folder. This change needs to be applied in `inbound`.

```

{
  "inbounds": [{
    "port": "PORTPORT", 
    "listen": "127.0.0.1",
    "tag": "socks-inbound",
    "protocol": "socks",
    "settings": {
...
```
And also apply this change in `outbound`.

```
{
"outbounds": [
   {
   "protocol": "vmess",
   "settings": {
     "vnext": [{
       "address": "IP.IP.IP.IP",
...
```

Now, for ease of work, some examples of configuration templates that iSegaro has worked hard to present; You can choose one according to your needs.

* Be careful, in these structures, only in the `outbounds` part, you should change the configuration specifications including 5 parts `Port, UUID, PATH, HOST, SNI`, which are marked with the word `xxxxx`, so wherever there is the word `xxxxx`, change it only depending on your configuration. And do not change the rest of the codes.

- Example template for Vmess+WS+TLS :

```
{
  "inbounds": [{
    "port": "PORTPORT", 
    "listen": "127.0.0.1",
    "tag": "socks-inbound",
    "protocol": "socks",
    "settings": {
      "auth": "noauth",
      "udp": false,
      "ip": "127.0.0.1"
    },
    "sniffing": {
      "enabled": true,
      "destOverride": ["http", "tls"]
    }
  }],
  "outbounds": [
    {
    "protocol": "vmess",
    "settings": {
      "vnext": [{
        "address": "IP.IP.IP.IP", 
        "port": xxxxx,
        "users": [{"id": "xxxxx" }]
      }]
    },
		"streamSettings": {
        "network": "ws",
        "security": "tls",
        "wsSettings": {
            "headers": {
                "Host": "xxxxx"
            },
            "path": "xxxxx"
        },
        "tlsSettings": {
            "serverName": "xxxxx",
            "allowInsecure": false,
			"fingerprint": "chrome",
			"alpn": [
			"http/1.1"
			]
        }
    }
	}],
  "other": {}
}
```

- Example template for Vless+GRPC+TLS :

```
{
  "inbounds": [{
    "port": "PORTPORT", 
    "listen": "127.0.0.1",
    "tag": "socks-inbound",
    "protocol": "socks",
    "settings": {
      "auth": "noauth",
      "udp": false,
      "ip": "127.0.0.1"
    },
    "sniffing": {
      "enabled": true,
      "destOverride": ["http", "tls"]
    }
  }],
  "outbounds": [
    {
    "protocol": "vless",
    "settings": {
      "vnext": [{
        "address": "IP.IP.IP.IP", 
        "port": xxxxx,
        "users": [{"id": "xxxxx",
		"encryption": "none"
			}]
      }]
    },
		"streamSettings": {
        "network": "grpc",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "serverName": "xxxxx",
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome"
        },
        "grpcSettings": {
          "serviceName": "",
          "multiMode": false
        }
      }
	}],
  "other": {}
}
```

- Example template for Trojan+WS+TLS :

```
{
  "inbounds": [{
    "port": "PORTPORT", 
    "listen": "127.0.0.1",
    "tag": "socks-inbound",
    "protocol": "socks",
    "settings": {
      "auth": "noauth",
      "udp": false,
      "ip": "127.0.0.1"
    },
    "sniffing": {
      "enabled": true,
      "destOverride": ["http", "tls"]
    }
  }],
  "outbounds": [
    {
      "tag": "proxy",
      "protocol": "trojan",
      "settings": {
        "servers": [
          {
            "address": "IP.IP.IP.IP",
            "method": "chacha20",
            "ota": false,
            "password": "xxxxx",
            "port": xxxxx,
            "level": 1,
            "flow": ""
          }
        ]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "serverName": "xxxxx",
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome"
        },
        "wsSettings": {
          "path": "xxxxx",
          "headers": {
            "Host": "xxxxx"
          }
        }
      },
      "mux": {
        "enabled": false,
        "concurrency": -1
      }
    }
  ],
  "other": {}
}
```

- Example template for Vless+WS+TLS :

```
{
"inbounds": [{
    "port": "PORTPORT", 
    "listen": "127.0.0.1",
    "tag": "socks-inbound",
    "protocol": "socks",
    "settings": {
      "auth": "noauth",
      "udp": false,
      "ip": "127.0.0.1"
    },
    "sniffing": {
      "enabled": true,
      "destOverride": ["http", "tls"]
    }
  }],
  "outbounds": [
    {
      "tag": "proxy",
      "protocol": "vless",
      "settings": {
        "vnext": [{
        "address": "IP.IP.IP.IP", 
        "port": xxxxx,
        "users": [{"id": "xxxxx",
		"encryption": "none"
			}]
      }]
      },
      "streamSettings": {
        "network": "ws",
        "security": "tls",
        "tlsSettings": {
          "allowInsecure": false,
          "serverName": "xxxxx",
          "alpn": [
            "http/1.1"
          ],
          "fingerprint": "chrome"
        },
        "wsSettings": {
          "path": "xxxxx",
          "headers": {
            "Host": "xxxxx"
          }
        }
      }
    }
  ],
	"other": {}
}
```

Finally, present your configuration according to the examples for the next step or use the default configuration.




</details>

Now suppose you have completed the prerequisites; All you need is the config file of the sample program or the config file created by yourself, which is in Json format; From the menu `Tools > Add custom v2ray config`, put it in the program so that the scan is done based on it, otherwise the program will scan with the default configuration.

![App](https://user-images.githubusercontent.com/125398461/234803794-7c7f5bb9-0967-4f1b-b519-9db266b7a0e7.png)

1. From `Tools > Add custom v2ray config`, you can give the desired file according to the described pattern to the software so that the scan can be done based on it.

2. You can specify the download or upload test type or both.

3. In this section, you can specify the number of simultaneous IPs to be tested by the scanner. It is suggested to increase this number step by step and increase or decrease it based on the CPU processing power of your system. Its default value is 4.

4. The fastest IP will be displayed after the scan is completed

5. The range of tested IPs is displayed

6. From this section, you can give the software the IP range you want to scan based on it.

* **Suggestion:** You can set the software to scan the entire default IP range once. For the next time, you can just scan this output (with higher accuracy), you will probably get a better result. Also, if you take an upload test, you will probably get a better result. All this depends on your efforts and creativity.

</details>
<br>
<br>

***
<br>
<br>

## Using Vahid Farid's scanner

<br>
<br>

***
<br>
<br>

## Using Safa Safarian's scanner

<br>
<br>

***
<br>
<br>

## What to do after finding a clean IP?
After finding a clean IP; You can register it with a DNS record without . That is, create a subdomain on Cloudflare. Turn off the proxy and enter the IP.

![PICTURE](https://user-images.githubusercontent.com/125398461/234565984-a2560018-7106-421f-850d-fb9db5687b26.png)

If you need more information about the domain, [click here](https://github.com/hiddify/hiddify-config/wiki/Domain-types-and-how-to-register-them).



Then in the Hiddify panel, you can put it in the CDN domain settings in the `Force to use host field in the CDN configuration`. [More details](https://github.com/hiddify/hiddify-config/wiki/How-to-configure-Hiddify-Panel-properly#cdn-domain)

![Screenshot_20230427_0656192](https://user-images.githubusercontent.com/125398461/234752684-280b90e8-0b00-4106-b744-b06117821b0f.png)
