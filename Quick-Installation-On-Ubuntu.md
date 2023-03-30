<div dir="rtl">

[فارسی](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%B5%D8%A8-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D8%A7%D9%88%D8%A8%D9%88%D9%86%D8%AA%D9%88)
</div>

# Before installation

If you have important information or an important service, note that installing this configuration may interfere with your other services. Therefore, please do not install any special service on your server.

This code is only applicable on Ubuntu and has been tested only on version 20.04 and 22.04.



Complete installation training video

In the video below, all the steps are described in full detail. This video is in Farsi and if you watch the steps you can handle that. Although We are considering making some English videos for non-Persian people, till then you can visit this or follow the instructions in this article.

<div align=center>

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/_LYFqrXVupI/0.jpg)](https://www.youtube.com/watch?v=_LYFqrXVupI)
</div>

# Installation steps on Ubuntu
1. Connect to your server through ssh and copy and run the following command in the terminal

```
sudo apt update&&sudo apt install curl&& sudo bash -c "$(curl -Lfo- https://raw.githubusercontent.com/hiddify/hiddify-config/main/common/download_install.sh)"
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
