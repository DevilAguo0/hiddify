<div dir="rtl">

[**![flag_of_Iran](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%B5%D8%A8-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D8%A7%D9%88%D8%A8%D9%88%D9%86%D8%AA%D9%88)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/hiddify/hiddify-config/wiki/All-tutorials-and-videos"><img width="100" src="https://github.com/hiddify/hiddify-config/assets/125398461/8ac5b906-105c-4b98-acf5-0e12e39e33f6" /></a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</div><br><br><div align=center>[![](https://img.shields.io/badge/Install%20On-Hetzner-D50C2D?style=flat-square&logo=Hetzner)](https://github.com/hiddify/Hiddify-Manager/wiki/Quick-installation-on-Hetzner-Servers)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![](https://img.shields.io/badge/Install%20On-Vultr-007BFC?style=flat-square&logo=vultr)](https://github.com/hiddify/Hiddify-Manager/wiki/Quick-installation-on-Vultr-Servers)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![](https://img.shields.io/badge/Install%20On-Oracle%20Cloud-F80000?style=flat-square&logo=oracle)](https://github.com/hiddify/Hiddify-Manager/wiki/Quick-Installation-on-Oracle-Cloud)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![](https://img.shields.io/badge/Install%20On-OVH-123F6D?style=flat-square&logo=ovh)](https://github.com/hiddify/Hiddify-Manager/wiki/Quick-Installation-on-OVH-Servers)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[![](https://img.shields.io/badge/Install%20On-Azure-0078D4?style=flat-square&logo=microsoft-azure)](https://github.com/hiddify/Hiddify-Manager/wiki/Quick-Installation-on-Microsoft-Azure)
</div>
<br>

# Quick installation on Ubuntu

## Before installation

If you have important information or an important service, note that installing this configuration may interfere with your other services. Therefore, please do not install any special service on your server.

This code is only applicable on Ubuntu and has been tested only on version 22.04.

- If you get your server directly from famous data centers; we made it easy and automated for you. In this method, the installation is done automatically very quickly and easily without the need for technical knowledge. Click on one of the buttons above. If not, follow this instruction to the end.

## Installation prerequisites
Before installation, you need a series of prerequisites which you can read them [here](https://github.com/hiddify/Hiddify-Server/wiki/Installation-prerequisites). 



## Complete installation training video

In the video below, all the steps are described in full detail. This video is in Farsi and if you watch the steps you can handle that. Although We are considering making some English videos for non-Persian people, till then you can visit this or follow the instructions in this article.

<!--
<div align=center>

<a href="https://www.youtube.com/watch?v=_LYFqrXVupI" >
 <img width="60%" src="https://user-images.githubusercontent.com/125398461/229776443-bde03106-275d-4eeb-8f37-a300ed96d55d.png" />
</a>
</div>
-->
## Installation steps on Ubuntu
1. Connect to your server through ssh and copy and run the following command in the terminal

```
sudo apt update&&sudo apt install -y curl&& sudo bash -c "$(curl -Lfo- https://raw.githubusercontent.com/hiddify/hiddify-config/main/common/download_install.sh)"
```

Congratulations, the installation is complete. 


2. After installation
At the end, a link will be generated which is the link to setup your proxy. Now we need to set the domain. Click on [this link](https://github.com/hiddify/hiddify-config/wiki/Guide-for-setting-up-the-domain-and-finalizing-the-installation) to complete the installation.

3. How to update 
For manual update, copy and run the following command in the terminal.

```
cd /opt/hiddify-config
sudo bash update.sh
```

For making the best use of this panel please view this [article](https://github.com/hiddify/hiddify-config/wiki/How-to-configure-Hiddify-Panel-properly).
