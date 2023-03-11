
<div dir="ltr" markdown="1">

### [For English version click here](https://github.com/hiddify/hiddify-config/wiki/Home-en)
</div>

<div dir="rtl" markdown="1">


***
[راهنمای نصب](https://github.com/hiddify/hiddify-config/wiki#%D8%B1%D8%A7%D9%87%D9%86%D9%85%D8%A7%DB%8C-%D9%86%D8%B5%D8%A8) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
[دموی سیستم](https://github.com/hiddify/hiddify-config/wiki#%D8%AF%D9%85%D9%88%DB%8C-%D8%B3%DB%8C%D8%B3%D8%AA%D9%85) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
[سوالات رایج](https://github.com/hiddify/hiddify-config/discussions/categories/q-a-%D8%B3%D9%88%D8%A7%D9%84%D8%A7%D8%AA-%D8%B1%D8%A7%DB%8C%D8%AC) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
[گزارش اشکالات](https://github.com/hiddify/hiddify-config/issues)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;


[کانال تلگرام](https://t.me/hiddify) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[آموزش پنل](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D9%BE%DB%8C%DA%A9%D8%B1%D8%A8%D9%86%D8%AF%DB%8C-%D9%BE%D9%86%D9%84-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[گروه تلگرام رفع اشکال](https://t.me/hiddify_board)
***



## معرفی
[ویدیو معرفی کامل](https://youtu.be/-a4tfRUsrNY)

پنل گذر از فیلترینگ چند کاربره‌ی هیدیفای، با امکان نصب خیلی راحت و نصب بیش از ۲۰ پروتوکل گذر از فیلترینگ و پروکسی تلگرام


<details markdown="1"> <summary>کانفیگ‌های پشتیبانی شده</summary> 

| کانفیگ های پشتیبانی شده | Supported Configs |
| - | - |
| ♥ **Telegram Proxy** ♥ | **vless+xtls** |
| **Web Socket (cdn support)**:<br> - vless+tls+ws <br>- trojan+tls+ws <br> - vmess+tls+ws | **h2+tls**:<br> - vless+tls<br> - trojan+tls<br> - vmess+tls |
| **grpc+tls**:<br> - vless+grpc+tls<br> - trojan+grpc+tls<br> - vmess+grpc+tls | **http1.1+tls**:  <br>- trojan+tls <br> - vmess+tls|
| **old configs**: <br> - trojango (cdn support) <br> - v2ray+ws (cdn support) <br> - vmess (cdn support) <br> - ss+faketls| **HTTP** <br> -unsafe, default is disable <br> - vless<br> -vmess |

</details>


<details markdown="1"> <summary>پروکسی هوشمند برای سایت های غیر ایرانی و فیلترشده</summary>
 
با استفاده از کلاینت کلش و پنل هایدیفای می‌تونین در ۳ حالت به اینترنت وصل بشید. 

۱. روش اول فقط سایت فیلترشده را از فیلترشکن عبور دهد.

۲. فقط سایت های ایرانی بدون فیلترشکن باز شود (پیشنهادی)

۳. تمام سایت ها از فیلترشکن عبور کنند

از طرف دیگر سعی شده راه‌حل ارائه شده در برابر کشف توسط نهادهای فیلتر کننده اینترنت مقاوم باشد و جلوی حملات معمول به سرور گرفته و امکان شناسایی حداقل باشد با این وجود فراموش نکنید که سایر پورت ها به جز ۲۲، ۸۰ و ۴۴۳ را غیر فعال کنید

</details>

<details markdown="1"><summary>سایر امکانات</summary>


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

<details markdown="1"> <summary>DNS over HTTPS (CDN support)</summary>
 
 برای استفاده از DNS over HTTPS کافی است در مرورگر از dns زیر استفاده کنید:
 
 `https://yourdomain.com/yoursecret/dns/dns-query{?dns}`
 
</details>

<details markdown="1"> <summary>Redirector (CDN support)</summary> 
  وقتی میخواهید پروکسی تلگرام یا پروکسی شدوساکس را از طریق برنامه های دیگر به اشتراک بگذارید امکان ریدایرکت با پشتیبانی سی دی ان فراهم می شود. برای مثال اگر کانفیگ شدوساکس را به جای fullURL قرار دهید باعث میشود با کلیک بر روی این لینک، اپ شدوساکس باز شده و پروکسی بر روی آن فعال شود. برای مثال:
 
 `https://yourdomain.com/yoursecret/redirect/fullURL` 
 

"fullURL" را با کانفیگ Shadowsocks جایگزین کنید:
 
 `https://yourdomain.com/yoursecret/redirect/ss://secret/` 
 
</details>


</details>
</details>

## راهنمای نصب


##### راهنمای نصب سریع و آسان بدون نیاز به دانش فنی و ssh

- [نصب در ولتر Vultr (گزینه پیشنهادی برای شروع ) ](https://github.com/hiddify/hiddify-config/wiki/Vultr-%D9%86%D8%B5%D8%A8-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D9%88%D9%84%D8%AA%D8%B1)
- [نصب در اوراکل کلود (چهار سرور رایگان)](https://github.com/hiddify/hiddify-config/wiki/Oracle-نصب-خیلی-خیلی-سریع-در-اوراکل-کلود)
- [نصب در OVH ](https://github.com/hiddify/hiddify-config/wiki/OVH-نصب-خیلی-سریع-در-او-وی-اچ)
- [نصب در هتزنر](https://github.com/hiddify/hiddify-config/wiki/Hetzner-نصب-خیلی-سریع-در-هتزنر)

##### راهنمای نصب در سرور از پیش آماده اوبونتو با ssh

- [نصب با یک دستور در سرور اوبونتو](https://github.com/hiddify/hiddify-config/wiki/نصب-سریع-در-اوبونتو)
- [نصب با داکر](https://github.com/hiddify/hiddify-config/wiki/نصب-با-داکر)


<details  markdown="1"> <summary>code for cloud-init</summary>

در بعضی از سایت‌های ارائه دهنده سرور، میتوانید با استفاده از اسکریپت زیر به صورت خودکار پروکسی را نصب کنید (به عنوان نمونه آموزش [هتزنر ](https://github.com/hiddify/hiddify-config/wiki/Hetzner-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D9%87%D8%AA%D8%B2%D9%86%D8%B1) و [OVH ](https://github.com/hiddify/hiddify-config/wiki/OVH-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D8%A7%D9%88-%D9%88%DB%8C-%D8%A7%DA%86) را مشاهده کنید) و از آدرس  `https://yourip.sslip.io`یا `http://yourip` لینک صفحه کاربران را مشاهده کنید کافی است به جای yourip آی پی خود را قرار دهید.

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
</div>

</details>




## دموی سیستم
<div align="center" markdown="1">

<img width="50%" src="https://user-images.githubusercontent.com/114227601/218550439-52299d0a-3b3e-4054-a742-528ee3cf5810.png" />
<img width="50%" src="https://user-images.githubusercontent.com/114227601/218550551-8caa38b8-6ffc-4c6d-93e2-3d3fe224d362.png" />

</div>

</div>










</div>