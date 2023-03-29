# Quick installation on Vultr Servers


Complete installation training video

In the video below, all the steps, including proxy installation and domain and subdomain settings, are described in full detail. This video is in Farsi and if you watch the steps you can get by that. We are considering making some English videos for non-Persian people. Till then you can visit this or follow the instructions in this article.

For using Vultr site and services please use VPN Connection if you live in countries with sanctions enforced, otherwise your account will be closed.

[![vultr](https://img.youtube.com/vi/hRRg10BURJI/maxresdefault.jpg)](https://www.youtube.com/watch?v=hRRg10BURJI)

## Proxy installation steps

1. At the operating system selection stage, be sure to select Ubuntu 22.04.

2. Copy the code below.

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
  - cd hiddify-config
 # uncomment it for using a special secret other wise it will be createed automatically
 # - echo "USER_SECRET=0123456789abcdef0123456789abcdef" >config.env
 # - echo "MAIN_DOMAIN=" >>config.env
  - echo "TELEGRAM_AD_TAG=" >>config.env
  - bash install.sh

final_message: "The system is finally up, after $UPTIME seconds"
output: { all: "| tee -a /root/cloud-init-output.log" }

# you can see the generated link from the website by using http://yourip/ or https://yourip.sslip.io in one hour, after that, it will be disapear. 
```

3. In the server section, check the Enable Cloud-Init User-Data option and put the copied code in it. After a maximum of 10 to 15 minutes, your proxy will be active.

![Group 1](https://user-images.githubusercontent.com/79760104/221190008-239cd200-4184-4c05-82ea-ff00a47e920e.jpg)

4. Now you need to set the domain. Click on [this link](https://github-com.translate.goog/hiddify/hiddify-config/wiki/%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D9%87%D8%A7%DB%8C%DB%8C-%DA%A9%D8%B1%D8%AF%D9%86-%D9%86%D8%B5%D8%A8?_x_tr_sl=fa&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=wapp) to complete the installation.