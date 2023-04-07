[**![World Learning Splash Image](https://user-images.githubusercontent.com/125398461/229074810-599bd7f9-0bc1-44a9-b76e-90bf7e182314.png) English**](https://github.com/hiddify/hiddify-config/wiki/Quick-installation-on-Hetzner-Servers)

<div dir="rtl" markdown="1">
 <!-- [آموزش گرفتن اکانت هتزنر از صفر تا صد](https://www.youtube.com/watch?v=XfS2Y6hZkqw) -->


# نصب خیلی سریع در Hetzner

</div>

<!--

<div align=center>

**فیلم آموزش هتزنر از صفر تا صد**
[![Hetzner](https://img.youtube.com/vi/vQ-NAfRXTZo/maxresdefault.jpg)](https://www.youtube.com/watch?v=vQ-NAfRXTZo)

</div>
—->
<div dir="rtl">
مراحل نصب:

- ابتدا وارد اکانت خود شوید و یک سرور جدید درست کنید.
</div>

<div align=center>

![image](https://user-images.githubusercontent.com/114227601/206861285-58832cec-a2a3-441e-91d4-8300d16584d6.png)

</div>
<div dir="rtl">

- حالا کد زیر را کپی کنید
</div>
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
  - git clone https://github.com/hiddify/hiddify-config/
  - cd hiddify-config
  - bash install.sh

final_message: "The system is finally up, after $UPTIME seconds"
output: { all: "| tee -a /root/cloud-init-output.log" }

# you can see the generated link from the website by using http://yourip/ or https://yourip.sslip.io in one hour, after that, it will be disapear. 
```

</div>

<div dir="rtl">

- کد بالا را در محل نشان داده در عکس قرار دهید.

</div>

<div align=center>

![image](https://user-images.githubusercontent.com/114227601/206861304-656682b4-17a3-44c1-89f9-7b0d89566728.png)

</div>

<div dir="rtl">

* پس از حداکثر 10 تا 15 دقیقه سرور شما آماده و پروکسی فعال خواهد بود. مطابق عکس آی پی خود را کپی کنید و در مرورگر باز کنید.

</div>

<div align=center>

![image](https://user-images.githubusercontent.com/114227601/206861323-1de41700-6ce4-403a-a644-0836e2a22876.png)

</div>

<div dir="rtl">

یادتون نره حداقل 10 دقیقه  صبر کنید

* حالا باید دامنه را تنظیم کنیم. بر روی [این لینک](https://github.com/hiddify/hiddify-config/wiki/%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D9%87%D8%A7%DB%8C%DB%8C-%DA%A9%D8%B1%D8%AF%D9%86-%D9%86%D8%B5%D8%A8) کلیک کنید تا نصب را نهایی کنید.

برای اینکه حداکثر استفاده را از مزایای این پنل ببرید؛ این [راهنما](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D9%BE%DB%8C%DA%A9%D8%B1%D8%A8%D9%86%D8%AF%DB%8C-%D9%BE%D9%86%D9%84-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C) را مطالعه کنید.

</div>