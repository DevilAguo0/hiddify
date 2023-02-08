
<div dir="rtl" markdown="1">

<div dir="ltr" markdown="1">

### [For English version click here](https://github.com/hiddify/hiddify-config/wiki/Home-en)
</div>

## فهرست مطالب

<details markdown="1"> <summary>توضیحات پروژه هایدیفای</summary>
<blockquote>
<details markdown="1"> <summary>پروژه متن‌باز</summary> 


کلیه سورس کدها در [گیت هاب](https://github.com/hiddify/hiddify-config) 
</details>

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


 <details markdown="1"> <summary>مقاوم در برابر کشف توسط فیلترچی</summary>
 
 سعی شده جلوی حملات معمول به سرور گرفته شود و امکان شناسایی حداقل باشد با این وجود فراموش نکنید که سایر پورت ها به جز 22، 80 و 443 را غیر فعال کنید

</details>

<details  markdown="1"> <summary>سیستم‌عامل‌های پشتیبانی شده</summary>
هایدیفای روی اوبونتو ۲۰.۰۴ و ۲۲.۰۴ تست شده است.
Ubuntu arm64 or amd64
</details>

</details>
</blockquote>

<details  markdown="1"> <summary>امکانات پنل هایدیفای</summary>
<blockquote>

<details markdown="1"> <summary>ارائه گزارش وضعیت سرویس </summary>
نمایش میزان مصرف پروکسی و تعداد کاربران،  بر اساس،پروتوکل، شهر و اپراتور اینترنت با حفظ حریم خصوصی کاربران

از طریق لینک زیر میتوانید مشاهده کنید وضعیت سرور رو

`https://yourdomain.com/yoursecret/stats/` 
</details>

<details  markdown="1"> <summary>به روز رسانی خودکار</summary>

به صورت پیش فرض به روزرسانی خودکار فعال است
جهت غیرفعال کردن آن کد زیر را در `config.env` اضافه کنید
```
ENABLE_AUTO_UPDATE=false
```
</details>
<details  markdown="1"> <summary>تست سرعت</summary>

از این طریق میتوان سرعت سرور بدون فیلترشکن و با فیلترشکن را بررسی کرد

![image](https://user-images.githubusercontent.com/114227601/210183115-4e1f4186-421e-4316-8082-3ce53275adc7.png)

</details>

</blockquote>
</details>

<details markdown="1"> <summary>آموزش نصب خیلی سریع در OVH, Oracle, Hetzner, Vultr بدون نیاز به ssh و دانش فنی</summary>

- [نصب خیلی خیلی سریع در ولتر Vultr (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/Vultr-نصب-خیلی-خیلی-سریع-در-ولتر)
- [راه اندازی 4 سرور رایگان در اوراکل کلود (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/Oracle-نصب-خیلی-خیلی-سریع-در-اوراکل-کلود)
- [آموزش نصب خیلی خیلی سریع در OVH (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/OVH-نصب-خیلی-سریع-در-او-وی-اچ)
- [آموزش نصب خیلی خیلی سریع در هتزنر (بدون ssh)](https://github.com/hiddify/hiddify-config/wiki/Hetzner-نصب-خیلی-سریع-در-هتزنر)

</details>

<details markdown="1"> <summary>آموزش نصب در سرور از پیش آماده اوبونتو با ssh</summary>

- [نصب سریع با یک دستور در سرور اوبونتو](https://github.com/hiddify/hiddify-config/wiki/نصب-سریع-در-اوبونتو)
- [نصب با داکر](https://github.com/hiddify/hiddify-config/wiki/نصب-با-داکر)

</details>
<details  markdown="1"> <summary>code for cloud-init</summary>

در بعضی از شرکت ها شما میتوانید با استفاده از اسکریپت زیر به صورت خودکار پروکسی را نصب کنید و از آدرس  `https://yourip.sslip.io/`یا `http://yourip/` لینک صفحه کاربران را مشاهدهد کنید کافی است به جای yourip آی پی خود را قرار دهید.

ضمنا این لینک موقت فقط به مدت یک ساعت فعال خواهد بود و پس از آن غیرفعال خواهد شد

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


 <details markdown="1"> <summary>صفحات راهنمای کاربران</summary> 
 
 با امکان تولید qrcode

 ![صفحه راهنمای کاربران](https://user-images.githubusercontent.com/114227601/206908372-db1fc206-4c6a-4206-ad39-e6b6b44a55c4.png)

</details>













