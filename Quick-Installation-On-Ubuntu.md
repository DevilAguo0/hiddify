# Before installation

If you have important information or an important service, note that installing this configuration may interfere with your other services. Therefore, please do not install any special service on your server.

This code is only applicable on Ubuntu and has been tested only on version 20.04 and 22.04.



Complete installation training video

In the video below, all the steps, including proxy installation and domain and subdomain settings, are described in full detail. This video is in Farsi and if you watch the steps you can get by that. We are considering making some English videos for non-Persian people. Till then you can visit this or follow the instructions in this article.

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
At the end, a link will be generated which is the link to setup your proxy. Now we need to set the domain. Click on [this link](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D9%87%D8%A7%DB%8C%DB%8C-%DA%A9%D8%B1%D8%AF%D9%86-%D9%86%D8%B5%D8%A8?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp) to complete the installation.

3. How to update 
For manual update, copy and run the following command in the terminal.

```
cd /opt/hiddify-config
sudo bash update.sh
```

For making the best use of this panel please view this [article]().
