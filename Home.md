<div dir="ltr" markdown="1">

### [For English version click here](https://github.com/hiddify/hiddify-config/wiki/Home-en)
</div>

<div dir="rtl" markdown="1">

پنل گذر از فیلترینگ چند کاربره‌ی هیدیفای، با امکان نصب خیلی راحت و نصب بیش از 20 پروتوکل گذر از فیلترینگ + پروکسی تلگرام

| [سوالات رایج](https://github.com/hiddify/hiddify-config/discussions) | [کانال تلگرام ما](https://t.me/hiddify) | [راهنمای نصب](https://github.com/hiddify/hiddify-config/wiki#%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D9%86%D8%B5%D8%A8)|  [دموی سیستم](https://github.com/hiddify/hiddify-config/wiki#%D8%AF%D9%85%D9%88%DB%8C-%D8%B3%DB%8C%D8%B3%D8%AA%D9%85)|
| -----|----|----|----|




## فهرست مطالب

### توضیحات پروژه هایدیفای


<details markdown="1"> <summary>کانفیگ‌های پشتیبانی شده</summary> 

| کانفیگ های پشتیبانی شده | Supported Configs |
| - | - |
| ♥ **Telegram Proxy** ♥ | **vless+xtls** |
| **Web Socket (cdn support)**:<br> - vless+tls+ws <br>- trojan+tls+ws <br> - vmess+tls+ws | **h2+tls**:<br> - vless+tls<br> - trojan+tls<br> - vmess+tls |
| **grpc+tls**:<br> - vless+grpc+tls<br> - trojan+grpc+tls<br> - vmess+grpc+tls | **http1.1+tls**:  <br>- trojan+tls <br> - vmess+tls|
| **old configs**: <br> - trojango (cdn support) <br> - v2ray+ws (cdn support) <br> - vmess (cdn support) <br> - ss+faketls| **HTTP** <br> -unsafe, default is disable <br> - vless<br> -vmess |

</details>

<details markdown="1"> <summary>پروکسی هوشمند برای سایت های غیر ایرانی و فیلترشده</summary>
 
با استفاده از کلاینت کلش و کانفیگ هایدیفای میتوانید در ۳ حالت به اینترنت وصل بشید. 

۱. روش اول فقط سایت فیلترشده را از فیلترشکن عبور دهد.

۲. فقط سایت های ایرانی بدون فیلترشکن باز شود (پیشنهادی)

۳. تمام سایت ها از فیلترشکن عبور کنند
</details>

<details markdown="1"><summary>سایر امکانات</summary>
 <details markdown="1"> <summary>مقاوم در برابر کشف توسط فیلترچی</summary>
 
 سعی شده جلوی حملات معمول به سرور گرفته شود و امکان شناسایی حداقل باشد با این وجود فراموش نکنید که سایر پورت ها به جز 22، 80 و 443 را غیر فعال کنید

</details>

<details  markdown="1"> <summary>سیستم‌عامل‌های پشتیبانی شده</summary>
هایدیفای روی اوبونتو ۲۰.۰۴ و ۲۲.۰۴ تست شده است.
Ubuntu arm64 or amd64
</details>



<details  markdown="1"> <summary>تست سرعت</summary>

از این طریق میتوان سرعت سرور بدون فیلترشکن و با فیلترشکن را بررسی کرد

![image](https://user-images.githubusercontent.com/114227601/210183115-4e1f4186-421e-4316-8082-3ce53275adc7.png)

</details>

 <details markdown="1"> <summary>صفحات راهنمای کاربران</summary> 
 با امکان تولید qrcode

 ![صفحه راهنمای کاربران](https://user-images.githubusercontent.com/114227601/206908372-db1fc206-4c6a-4206-ad39-e6b6b44a55c4.png)
</details>

<details markdown="1"> <summary>DNS over HTTPS (cdn support)</summary>
 
 برای استفاده از DNS over HTTPS کافی است در مرورگر از dns زیر استفاده کنید:
 
 `https://yourdomain.com/yoursecret/dns/dns-query{?dns}`
 
</details>

<details markdown="1"> <summary>Redirector (cdn support)</summary> 
 
 نکته این امر آن است که برای مثال وقتی میخواهید پروکسی تلگرام یا پروکسی شدوساکس را از طریق برنامه های دیگر به اشتراک بگذارید امکان آن فراهم می شود. برای مثال اگر کانفیگ شدوساکس را به جای `fullURL` آن قرار دهید باعث میشود با کلیک بر روی این لینک، نرم افزار شدوساکس باز شده و پروکسی بر روی آن فعال شود.
 
 `https://yourdomain.com/yoursecret/redirect/fullURL` 
 
 به عنوان مثال:
 
 `https://yourdomain.com/yoursecret/redirect/ss://secret/` 
 
</details>


</details>
</details>

### راهنمای نصب

##### آموزش نصب خیلی سریع در OVH, Oracle, Hetzner, Vultr بدون نیاز به ssh و دانش فنی

- [نصب خیلی خیلی سریع در ولتر Vultr (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/Vultr-نصب-خیلی-خیلی-سریع-در-ولتر)
- [راه اندازی 4 سرور رایگان در اوراکل کلود (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/Oracle-نصب-خیلی-خیلی-سریع-در-اوراکل-کلود)
- [آموزش نصب خیلی خیلی سریع در OVH (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/OVH-نصب-خیلی-سریع-در-او-وی-اچ)
- [آموزش نصب خیلی خیلی سریع در هتزنر (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/Hetzner-نصب-خیلی-سریع-در-هتزنر)

</details>

##### آموزش نصب در سرور از پیش آماده اوبونتو با ssh

- [نصب سریع با یک دستور در سرور اوبونتو](https://github.com/hiddify/hiddify-config/wiki/نصب-سریع-در-اوبونتو)
- [نصب با داکر](https://github.com/hiddify/hiddify-config/wiki/نصب-با-داکر)

</details>
<details  markdown="1"> <summary>code for cloud-init</summary>

در بعضی از شرکت ها شما میتوانید با استفاده از اسکریپت زیر به صورت خودکار پروکسی را نصب کنید (به عنوان نمونه آموزش [هتزنر ](https://github.com/hiddify/hiddify-config/wiki/Hetzner-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D9%87%D8%AA%D8%B2%D9%86%D8%B1) و [OVH ](https://github.com/hiddify/hiddify-config/wiki/OVH-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D8%A7%D9%88-%D9%88%DB%8C-%D8%A7%DA%86) را مشاهده کنید) و از آدرس  `https://yourip.sslip.io`یا `http://yourip` لینک صفحه کاربران را مشاهده کنید کافی است به جای yourip آی پی خود را قرار دهید.

ضمنا این لینک موقت فقط به مدت یک ساعت فعال خواهد بود و پس از آن غیرفعال خواهد شد

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

</details>

</div>


### دموی سیستم
- بخش کاربران
![image](https://user-images.githubusercontent.com/114227601/218550439-52299d0a-3b3e-4054-a742-528ee3cf5810.png)

- بخش مدیریت
![image](https://user-images.githubusercontent.com/114227601/218550551-8caa38b8-6ffc-4c6d-93e2-3d3fe224d362.png)











