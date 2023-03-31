<div dir="rtl" markdown="1">

 [**🇮🇷فارسی**](https://github.com/hiddify/hiddify-config/wiki/Home_Fa)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</div>
</br>
<div align=left markdown="1">

![Hiddify Logo](https://user-images.githubusercontent.com/125398461/227720391-f6360e48-f211-4f56-a5b1-42522c30ecb7.png)


</div>
</br>


<div dir="ltr" markdown="1">

## Welcome to Hiddify

Hiddify is a powerful and professional anti-censorship toolbox, which is a multi-user panel with an effortless installation and supporting more than 20 protocols to circumvent filtering plus telegram proxy.  It's optimized for censorship circumvention in China, Russia and Iran and recommended by [**xray**](https://github.com/XTLS/Xray-core). It's a great replacement of X-UI.

<details markdown="1"> <summary><b>Supported protocols</b></summary> 

| Supported Configs | Supported Configs |
| - | - |
| ♥ **Telegram Proxy** ♥ | **vless+xtls** |
| **Web Socket (cdn support)**:<br> - vless+tls+ws <br>- trojan+tls+ws <br> - vmess+tls+ws | **h2+tls**:<br> - vless+tls<br> - trojan+tls<br> - vmess+tls |
| **grpc+tls**:<br> - vless+grpc+tls<br> - trojan+grpc+tls<br> - vmess+grpc+tls | **http1.1+tls**:  <br>- trojan+tls <br> - vmess+tls|
| **old configs**: <br> - trojango (cdn support) <br> - v2ray+ws (cdn support) <br> - vmess (cdn support) <br> - ss+faketls| **HTTP** <br> -unsafe, default is disable <br> - vless<br> -vmess |

</details>


<details markdown="1"> <summary><b>Smart proxy for domestic and filtered sites</b></summary>
 
You can connect to the internet in 3 modes using Clash client and Hiddify panel. 
1. This method only circumvents the filtered websites via the anti-filter.
2. This method circumvents all websites except for the Iranian websites, and they can be opened without ant-filter (recommended)
3. This method circumvents all websites. 

At the same time, the proposed solution is resistant to detection by the internet filtering entities and prevents the usual attacks on the server i.e., the possibility of detection is minimal, however, do not forget to disable other ports except 22, 80 and 443.  

</details>

<details markdown="1"><summary><b>Other Fantastic Features</b></summary>


<details  markdown="1"> <summary>Supported operating systems</summary>
Hiddify has been tested on Ubuntu 20.04 and 22.04. Ubuntu arm64 or amd64
</details>



<details  markdown="1"> <summary>Speed test</summary>

In this way, you can check the speed of the server with and without VPN connection.

![image](https://user-images.githubusercontent.com/114227601/210183115-4e1f4186-421e-4316-8082-3ce53275adc7.png)

</details>

 

<details markdown="1"> <summary>DNS over HTTPS (CDN support)</summary>
 
To use DNS over HTTPS, just use the following DNS in the browser. 
 
 `https://yourdomain.com/yoursecret/dns/dns-query{?dns}`
 
</details>

<details markdown="1"> <summary>Redirector (CDN support)</summary> 
When you want to share Telegram proxy or Shadowsocks proxy through other programs, it is possible to redirect with CDN support. For example, if you put the Shadowsocks configuration instead of "fullURL", clicking on this link will open Shadowsocks app and activate the proxy on it. For example:
 `https://yourdomain.com/yoursecret/redirect/fullURL` 

 Replace "fullURL" by the Shadowsocks configuration. 

 
 `https://yourdomain.com/yoursecret/redirect/ss://secret/` 
 
</details>


</details>
</details>

<!--
<div align=center>


<a href="https://www.youtube.com/watch?v=-a4tfRUsrNY">
  <img width="50%" src="https://user-images.githubusercontent.com/125398461/227990194-e20b67dc-6cda-4b05-bd26-b7147d830a12.png" />
</a>
</div>

-->

## Installation Guide


<details markdown="1"> <summary><b>Installation without ssh</b></summary>
This way you can take advantage of quick and easy installation of this panel using cloud-init scripts with no technical knowledge and even without any ssh connections

- [Installation on Vultr (Recommended option to start) ](https://github.com/hiddify/hiddify-config/wiki/Quick-installation-on-Vultr-Servers)
- [Installation on Oracle Cloud](https://github.com/hiddify/hiddify-config/wiki/Quick-Installation-on-Oracle-Cloud)
- [Installation on OVH](https://github.com/hiddify/hiddify-config/wiki/Quick-Installation-on-OVH-Servers)
- [Installation on Hetzner](https://github.com/hiddify/hiddify-config/wiki/Quick-installation-on-Hetzner-Servers)
- [Installation on Microsoft Azure](https://github.com/hiddify/hiddify-config/wiki/Quick-Installation-on-Microsoft-Azure)

</details>

<details markdown="1"> <summary><b>Installation with ssh</b></summary>
Here you can use this guide on prepared Ubuntu server with ssh connection

- [Installation on Ubuntu server](https://github.com/hiddify/hiddify-config/wiki/Quick-Installation-On-Ubuntu)
- [Installation with Docker](https://github.com/hiddify/hiddify-config/wiki/Install-Hiddify-using-Docker)

</details>


## Configuration Guide
<b>Making the best use of this panel via [this guide](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D9%BE%DB%8C%DA%A9%D8%B1%D8%A8%D9%86%D8%AF%DB%8C-%D9%BE%D9%86%D9%84-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp).</b>

## Other Useful Guides

#### Guide to Domain Registration and Setup
For information on how to register a domain and set it up in Hidify, see [this link](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%D8%A7%D9%86%D9%88%D8%A7%D8%B9-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D8%AD%D9%88%D9%87-%D8%AB%D8%A8%D8%AA-%E2%80%8C%D8%A2%D9%86%E2%80%8C%D9%87%D8%A7?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp).

#### Guide to ensure the server IP is clean
If you want to make sure that the server's IP or domain is clean, read [this article](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D8%A7%D8%B7%D9%85%DB%8C%D9%86%D8%A7%D9%86-%D8%A7%D8%B2-%D8%AA%D9%85%DB%8C%D8%B2-%D8%A8%D9%88%D8%AF%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%DB%8C%D8%A7-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D8%B3%D8%B1%D9%88%D8%B1?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp) in the wiki.

#### Guide to find a clean Cloudflare IP
If you need to find clean IPs of Coldflare; Consider [this topic](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%DA%86%DA%AF%D9%88%D9%86%DA%AF%DB%8C-%DB%8C%D8%A7%D9%81%D8%AA%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%D8%AA%D9%85%DB%8C%D8%B2-%DA%A9%D9%84%D8%A7%D8%AF%D9%81%D9%84%D8%B1?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp).

#### Guide for setting up and using Workers
To use Workers service of Cloudflare, read [this guide](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%D8%A7%D9%86%D9%88%D8%A7%D8%B9-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D8%AD%D9%88%D9%87-%D8%AB%D8%A8%D8%AA-%E2%80%8C%D8%A2%D9%86%E2%80%8C%D9%87%D8%A7?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp).

#### Guide for Connecting and Setting up the Server through SSH
If you need to get information about how to connect to the server through ssh and configure it, see [this article](https://github-com.translate.goog/hiddify/hiddify-config/wiki/SSH-%D9%86%D8%AD%D9%88%D9%87-%D8%A7%D8%AA%D8%B5%D8%A7%D9%84-%D9%88-%D8%B1%D9%81%D8%B9-%D8%B9%DB%8C%D8%A8-%D8%A7%D8%B2-%D8%B7%D8%B1%DB%8C%D9%82?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp).

</br>

***
[FAQ](https://github.com/hiddify/hiddify-config/discussions/categories/q-a-%D8%B3%D9%88%D8%A7%D9%84%D8%A7%D8%AA-%D8%B1%D8%A7%DB%8C%D8%AC)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[ReportBugs](https://github.com/hiddify/hiddify-config/issues)&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Telegram Channel](https://t.me/hiddify) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[Telegram Group](https://t.me/hiddify_board/5)




</div>