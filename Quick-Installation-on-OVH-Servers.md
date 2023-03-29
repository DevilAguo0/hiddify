# Quick Installation on OVH Servers

Firstly you can watch this video in order to do that.

[![OVH](https://img.youtube.com/vi/06fMizOb-DE/maxresdefault.jpg)](https://www.youtube.com/watch?v=06fMizOb-DE)

# Installation steps
1. copy the following code:
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
  - bash install.sh

final_message: "The system is finally up, after $UPTIME seconds"
output: { all: "| tee -a /root/cloud-init-output.log" }

# you can see the generated link from the website by using http://yourip/ or https://yourip.sslip.io in one hour, after that, it will be disapear. 
```

Do not forget to wait at least 10 minutes.

2. Now we need to setup the domain and finalize the installation. [(visit this article)](r)

For making the best use of this panel please view this [article]().