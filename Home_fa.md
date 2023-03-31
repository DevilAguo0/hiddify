
<div dir="ltr" markdown="1">

[**🇺🇸English**](https://github.com/hiddify/hiddify-config/wiki)
</div>
</br>
<div align=right markdown="1">
  <img src="https://user-images.githubusercontent.com/125398461/227987559-b4732223-fa47-466c-8323-a8b7b1a5c687.png"/>
</div>
</br>
<div dir="rtl" markdown="1">



## به هیدیفای خوش آمدید
هیدیفای یک ابزار قدرتمند و خرفه ای ضدسانسور اینترنت است که دارای پنل چند کاربره و نصب آسان است و به شما کمک می کند با بیش از ۲۰ پروتکل پشتیبانی شده فیلترینگ اینترنت را دور بزنید همچنین می توانید از پروکسی تلگرام استفاده نمایید. این ابزار برای شبکه اینترنت ایران بهینه سازی شده است و توسط [**xray**](https://github.com/XTLS/Xray-core) توصیه شده است. این پنل یک جایگزین عالی برای X-UI می باشد.

<details markdown="1"> <summary><b>کانفیگ‌های پشتیبانی شده</b></summary> 

| کانفیگ های پشتیبانی شده | Supported Configs |
| - | - |
| ♥ **Telegram Proxy** ♥ | **vless+xtls** |
| **Web Socket (cdn support)**:<br> - vless+tls+ws <br>- trojan+tls+ws <br> - vmess+tls+ws | **h2+tls**:<br> - vless+tls<br> - trojan+tls<br> - vmess+tls |
| **grpc+tls**:<br> - vless+grpc+tls<br> - trojan+grpc+tls<br> - vmess+grpc+tls | **http1.1+tls**:  <br>- trojan+tls <br> - vmess+tls|
| **old configs**: <br> - trojango (cdn support) <br> - v2ray+ws (cdn support) <br> - vmess (cdn support) <br> - ss+faketls| **HTTP** <br> -unsafe, default is disable <br> - vless<br> -vmess |

</details>


<details markdown="1"> <summary><b>پروکسی هوشمند برای سایت های غیر ایرانی و فیلترشده</b></summary>
 
با استفاده از کلاینت کلش و پنل هایدیفای می‌تونین در ۳ حالت به اینترنت وصل بشید. 

۱. روش اول فقط سایت فیلترشده را از فیلترشکن عبور دهد.

۲. فقط سایت های ایرانی بدون فیلترشکن باز شود (پیشنهادی)

۳. تمام سایت ها از فیلترشکن عبور کنند

از طرف دیگر سعی شده راه‌حل ارائه شده در برابر کشف توسط نهادهای فیلتر کننده اینترنت مقاوم باشد و جلوی حملات معمول به سرور گرفته و امکان شناسایی حداقل باشد با این وجود فراموش نکنید که سایر پورت ها به جز ۲۲، ۸۰ و ۴۴۳ را غیر فعال کنید

</details>

<details markdown="1"><summary><b>سایر امکانات</b></summary>


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

</div>
<div align=center>


<a href="https://www.youtube.com/watch?v=-a4tfRUsrNY">
  <img width="50%" src="https://user-images.githubusercontent.com/125398461/227990194-e20b67dc-6cda-4b05-bd26-b7147d830a12.png" />
</a>
</div>


<div align=right dir="rtl">

## راهنمای نصب

<details markdown="1"> <summary><b>راهنمای نصب بدون ssh</b></summary> 
در این روش به صورت خیلی سریع و آسان بدون نیاز به دانش فنی و ssh و با استفاده از قابلیت cloud-init نصب انجام می شود.

- [نصب در ولتر Vultr (گزینه پیشنهادی برای شروع ) ](https://github.com/hiddify/hiddify-config/wiki/Vultr-%D9%86%D8%B5%D8%A8-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D9%88%D9%84%D8%AA%D8%B1)
- [نصب در اوراکل کلود (چهار سرور رایگان)](https://github.com/hiddify/hiddify-config/wiki/Oracle-نصب-خیلی-خیلی-سریع-در-اوراکل-کلود)
- [نصب در OVH ](https://github.com/hiddify/hiddify-config/wiki/OVH-نصب-خیلی-سریع-در-او-وی-اچ)
- [نصب در Hetzner](https://github.com/hiddify/hiddify-config/wiki/Hetzner-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1)
- [نصب در مایکروسافت Azure](https://github.com/hiddify/hiddify-config/wiki/Azure-%D9%86%D8%B5%D8%A8-%D8%AE%DB%8C%D9%84%DB%8C-%D8%AE%DB%8C%D9%84%DB%8C-%D8%B3%D8%B1%DB%8C%D8%B9-%D8%AF%D8%B1-%D9%85%D8%A7%DB%8C%DA%A9%D8%B1%D9%88%D8%B3%D8%A7%D9%81%D8%AA-%D8%A2%DA%98%D9%88%D8%B1)


</details>

<details markdown="1"> <summary><b>راهنمای نصب با ssh</b></summary>

در این حالت روی سرور از پیش آماده اوبونتو با ssh نصب انجام می شود.

- [نصب با یک دستور در سرور اوبونتو](https://github.com/hiddify/hiddify-config/wiki/نصب-سریع-در-اوبونتو)
- [نصب با داکر](https://github.com/hiddify/hiddify-config/wiki/نصب-با-داکر)




</details>






## راهنمای پیکربندی
برای اینکه حداکثر استفاده را از مزایای این پنل ببرید؛ این [راهنما](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D9%BE%DB%8C%DA%A9%D8%B1%D8%A8%D9%86%D8%AF%DB%8C-%D9%BE%D9%86%D9%84-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C) را مطالعه کنید.






</div>

</div>

<div dir="rtl" markdown="1">

## سایر راهنماهای مفید
#### راهنمای تنظیم دامنه
جهت اطلاع از نحوه ثبت دامنه و تنظیم آن در هیدیفای [این لینک](https://github.com/hiddify/hiddify-config/wiki/%D8%A7%D9%86%D9%88%D8%A7%D8%B9-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D8%AD%D9%88%D9%87-%D8%AB%D8%A8%D8%AA-%E2%80%8C%D8%A2%D9%86%E2%80%8C%D9%87%D8%A7) را ببینید.

#### راهنمای اطمینان از تمیز بودن‌آیپی سرور
جهت حصول اطمینان از تمیز بودن آیپی یا دامنه سرور [این مطلب](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D8%A7%D8%B7%D9%85%DB%8C%D9%86%D8%A7%D9%86-%D8%A7%D8%B2-%D8%AA%D9%85%DB%8C%D8%B2-%D8%A8%D9%88%D8%AF%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%DB%8C%D8%A7-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D8%B3%D8%B1%D9%88%D8%B1) را در ویکی مطالعه نمایید.

#### راهنمای یافتن آیپی تمیز کلادفلر
در صورتی که نیاز به یافتن آیپی های تمیز کلدفلر دارید؛ [این تاپیک](https://github.com/hiddify/hiddify-config/wiki/%DA%86%DA%AF%D9%88%D9%86%DA%AF%DB%8C-%DB%8C%D8%A7%D9%81%D8%AA%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%D8%AA%D9%85%DB%8C%D8%B2-%DA%A9%D9%84%D8%A7%D8%AF%D9%81%D9%84%D8%B1) را ملاظحه فرمایید.

#### راهنمای تنظیم و استفاده از ورکرز
جهت استفاده از سرویس ورکرز کلادفلر [این راهنما](https://github.com/hiddify/hiddify-config/wiki/%D8%A7%D9%86%D9%88%D8%A7%D8%B9-%D8%AF%D8%A7%D9%85%D9%86%D9%87-%D9%88-%D9%86%D8%AD%D9%88%D9%87-%D8%AB%D8%A8%D8%AA-%E2%80%8C%D8%A2%D9%86%E2%80%8C%D9%87%D8%A7) را مطالعه فرمایید.

#### راهنمای اتصال و تنظیم سرور از طریق ssh
در صورت نیاز به کسب اطلاع درباره نحوه ارتباط با سرور از طریق ssh و انجام تنظیمات آن [این مطلب](https://github.com/hiddify/hiddify-config/wiki/SSH-%D9%86%D8%AD%D9%88%D9%87-%D8%A7%D8%AA%D8%B5%D8%A7%D9%84-%D9%88-%D8%B1%D9%81%D8%B9-%D8%B9%DB%8C%D8%A8-%D8%A7%D8%B2-%D8%B7%D8%B1%DB%8C%D9%82) را ملاحظه فرمایید.

</div>

</br>

***
<div align=right>

[سوالات رایج](https://github.com/hiddify/hiddify-config/discussions/categories/q-a-%D8%B3%D9%88%D8%A7%D9%84%D8%A7%D8%AA-%D8%B1%D8%A7%DB%8C%D8%AC) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[گزارش اشکالات](https://github.com/hiddify/hiddify-config/issues)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[کانال تلگرام](https://t.me/hiddify) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[گروه تلگرام رفع اشکال](https://t.me/hiddify_board)

</div>