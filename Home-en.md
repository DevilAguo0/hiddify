


# Welcome to Hiddify 
# [جهت مشاهده توضیحات فارسی کلیک کنید](https://github.com/hiddify/hiddify-config/wiki/Home)



In this article, we will teach you how to create a dedicated multiprotocol filter on port 443.
Supported items:


| کانفیگ های پشتیبانی شده | Supported Configs |
| - | - |
| ♥ **Telegram Proxy** ♥ | **vless+xtls** |
| **Web Socket (cdn support)**:<br> - vless+tls+ws <br>- trojan+tls+ws <br> - vmess+tls+ws | **h2+tls**:<br> - vless+tls<br> - trojan+tls<br> - vmess+tls |
| **grpc+tls**:<br> - vless+grpc+tls<br> - trojan+grpc+tls<br> - vmess+grpc+tls | **http1.1+tls**:  <br>- trojan+tls <br> - vmess+tls|
| **old configs**: <br> - trojango (cdn support) <br> - v2ray+ws (cdn support) <br> - vmess (cdn support) <br> - ss+faketls| **HTTP** <br> -unsafe, default is disable <br> - vless<br> -vmess |




<details markdown="1"> <summary>DNS over HTTPS (cdn support)</summary>
 
  To use DNS over HTTPS, just use the following dns in the browser:
 
  `https://yourdomain.com/yoursecret/dns/dns-query{?dns}`
 
</details>
<details markdown="1"> <summary>Redirector (cdn support)</summary>
 
  The point of this is that, for example, when you want to share Telegram proxy or ShadowSax proxy through other programs, it is possible. For example, if you put the ShadowSax configuration instead of ``fullURL'', by clicking on this link, the ShadowSax software will be opened and the proxy will be activated on it.
 
  `https://yourdomain.com/yoursecret/redirect/fullURL`
 
  for example:
 
  `https://yourdomain.com/yoursecret/redirect/ss://secret/`
 
</details>
  <details markdown="1"> <summary>Smart proxy for non-Iranian and filtered sites </summary>
 
  You can connect to the Internet in 3 modes by using the Clash client and the configuration we made.

1- The first method only passes the filtered site through the filter breaker.

2- Only Iranian sites can be opened without a filter breaker (recommended)

3- All sites pass through the filter breaker

</details>
  <details markdown="1"> <summary>Resistant to detection by filters</summary>
 
  Attempts have been made to prevent common attacks on the server and to minimize the possibility of detection, however, do not forget to disable other ports except 22, 80 and 443.

</details>
  <details markdown="1"> <summary>User manual pages</summary>
 
  With the possibility of generating qrcode

  ![User manual page](https://user-images.githubusercontent.com/114227601/206908372-db1fc206-4c6a-4206-ad39-e6b6b44a55c4.png)

</details>
<details markdown="1"> <summary>Open Source</summary>

All source codes in [Git Hub] (https://github.com/hiddify/hiddify-config)
</details>

<details markdown="1"> <summary>Provide service status report </summary>
Display of proxy consumption and number of users, based on protocol, city and internet operator while maintaining users' privacy

You can see the status of the server through the link below

`https://yourdomain.com/yoursecret/stats/`

</details>
<details markdown="1"> <summary>Supported OS: Ubuntu arm64 or amd64</summary>
It is tested on Ubuntu 20.04 and 22.04
</details>

<details markdown="1"> <summary>Auto Up to date</summary>

Automatic update is enabled by default
To disable it, add the following code in `config.env`
```
ENABLE_AUTO_UPDATE=false
```
</details>


<details markdown="1"> <summary>code for cloud-init</summary>

In some companies, you can automatically install the proxy using the following script and see the link of the user page from the address ``https://yourip.sslip.io/'' or ``http://yourip/''. Put your IP instead of yourip.

Also, this temporary link will only be active for one hour and then it will be deactivated

```
#cloud-config
package_upgrade: true
packages:
   - apt-transport-https
   - ca-certificates
   - curl
   - wget
   - gnupg-agent
   - software-properties-common
   - git

runcmd:
   - cd /opt
   - git clone https://github.com/hiddify/hiddify-config/
   - cd hidedify-config
  # uncomment it for using a special secret otherwise it will be created automatically
  # - echo "USER_SECRET=0123456789abcdef0123456789abcdef" >config.env
  # - echo "MAIN_DOMAIN=" >>config.env
   - echo "TELEGRAM_AD_TAG=" >>config.env
   - bash install.sh

final_message: "The system is finally up, after $UPTIME seconds"
output: { all: "| tee -a /root/cloud-init-output.log" }

# you can see the generated link from the website by using http://yourip/ or https://yourip.sslip.io in one hour, after that, it will disappear.
```

</details>
<details markdown="1"> <summary>Built in speed test</summary>

In this way, you can check the speed of the server without filter breaker and with filter breaker

![image](https://user-images.githubusercontent.com/114227601/210183115-4e1f4186-421e-4316-8082-3ce53275adc7.png)

</details>

# [Our Telegram channel (click)](https://t.me/hiddify)

# learn inistallation

## Very fast installation training in OVH, Oracle, Hetzner, Vultr without the need for ssh and technical knowledge
- [Very, very fast installation in Vultr (without ssh)](https://github.com/hiddify/hiddify-config/wiki/Vultr-install-very-very-fast-in-voltr)
- [Setting up 4 free servers in Oracle Cloud (without ssh)](https://github.com/hiddify/hiddify-config/wiki/Oracle-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D8%A7%D9%88%D8%B1%D8%A7%DA%A9%D9%84-%DA%A9%D9%84%D9%88%D8%AF)
- [Tutorial to install very, very quickly in OVH (without ssh)](https://github.com/hiddify/hiddify-config/wiki/OVH-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D8%A7%D9%88-%D9%88%DB%8C-%D8%A7%DA%86)
- [Tutorial to install very, very quickly in Hetzner (without ssh)](https://github.com/hiddify/hiddify-config/wiki/Hetzner-installation-very-quick-in-Hetzner)

## How to install on pre-prepared Ubuntu server with ssh
- [Quick installation with one command on Ubuntu server](https://github.com/hiddify/hiddify-config/wiki/quick-installation-in-ubuntu)
- [Install with Docker](https://github.com/hiddify/hiddify-config/wiki/install-with-docker)


# Help page for users and admin

With the possibility of generating qrcode


![HiddifyPanel](https://raw.githubusercontent.com/hiddify/hiddify-config/main/docs/HiddifyPanel.webp)
<!--
![User manual page](https://user-images.githubusercontent.com/114227601/206908372-db1fc206-4c6a-4206-ad39-e6b6b44a55c4.png)


# Management page
![image](https://user-images.githubusercontent.com/114227601/209979538-cb3196aa-a832-4b06-95c4-37e9795e00cb.png)
-->
