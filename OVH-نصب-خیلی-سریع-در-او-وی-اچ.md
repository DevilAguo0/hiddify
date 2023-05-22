[**![World Learning Splash Image](https://user-images.githubusercontent.com/125398461/229074810-599bd7f9-0bc1-44a9-b76e-90bf7e182314.png) English**](https://github.com/hiddify/hiddify-config/wiki/Quick-Installation-on-OVH-Servers)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/hiddify/hiddify-config/wiki/%D9%87%D9%85%D9%87-%D8%A2%D9%85%D9%88%D8%B2%D8%B4%E2%80%8C%D9%87%D8%A7-%D9%88-%D9%88%DB%8C%D8%AF%D8%A6%D9%88%D9%87%D8%A7"><img width="100" src="https://github.com/hiddify/hiddify-config/assets/125398461/3704cd84-eee6-4c45-abe7-3c02936bbebb" /></a>
<div dir="rtl" markdown="1">

فیلم زیر را مشاهده کنید

[![OVH](https://img.youtube.com/vi/06fMizOb-DE/maxresdefault.jpg)](https://www.youtube.com/watch?v=06fMizOb-DE)



حالا کد زیر را کپی کنید

<div dir="ltr" markdown="1">

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
  - bash -c "$(curl -Lfo- https://raw.githubusercontent.com/hiddify/hiddify-config/main/common/download_install.sh)"

final_message: "The system is finally up, after $UPTIME seconds"
output: { all: "| tee -a /root/cloud-init-output.log" }

# you can see the generated link from the website by using http://yourip/ or https://yourip.sslip.io in one hour, after that, it will be disapear. 
```

</div>

یادتون نره حداقل 10 دقیقه  صبر کنیدا

حالا باید دامنه را تنظیم کنیم. بر روی [این لینک](https://github.com/hiddify/hiddify-config/wiki/%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D9%87%D8%A7%DB%8C%DB%8C-%DA%A9%D8%B1%D8%AF%D9%86-%D9%86%D8%B5%D8%A8) کلیک کنید تا نصب را نهایی کنید.

</div>