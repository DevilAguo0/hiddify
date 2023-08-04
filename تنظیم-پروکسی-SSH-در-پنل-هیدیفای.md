[**![Lang_Eng](https://user-images.githubusercontent.com/125398461/229074810-599bd7f9-0bc1-44a9-b76e-90bf7e182314.png) English**](https://github.com/hiddify/hiddify-config/wiki/SSH-proxy-setting-on-Hiddify-panel)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/hiddify/hiddify-config/wiki/%D9%87%D9%85%D9%87-%D8%A2%D9%85%D9%88%D8%B2%D8%B4%E2%80%8C%D9%87%D8%A7-%D9%88-%D9%88%DB%8C%D8%AF%D8%A6%D9%88%D9%87%D8%A7"><img width="100" src="https://github.com/hiddify/hiddify-config/assets/125398461/3704cd84-eee6-4c45-abe7-3c02936bbebb" /></a>

<div dir="rtl" markdown="1">

# تنظیم پروکسی SSH در پنل هیدیفای

همانطور که می‌دانید در نسخه ۸ پنل هیدیفای یک پروکسی برای سرویس SSH درست شده که هیچ‌گونه دسترسی به سرور ندارد و فقط می‌تواند به عنوان پروکسی استفاده شود. این پروکسی کاملا امن شده و هیچ فینگرپرینتی برای شناسایی ندارد. (به جز خود پروتکل SSH که استفاده عمومی دارد)

در ادامه با این آموزش همراه باشید تا با نحوه انجام تنظیمات آن در پنل هیدیفای آشنا شوید.

## انجام تنظیمات پروکسی SSH
ابتدا در `تنظیمات` پنل به بخش `پروکسی SSH` بروید.

<div align=center>

![SSH Proxy](https://github.com/hiddify/hiddify-config/assets/125398461/9ef5adf8-ea02-447f-87b4-1975a1a6db1e)

</div>

در اینجا می‌توانید پورت مورد نظر خود برای این سرویس را انتخاب نمایید. همچنین قابلیت فعال‌سازی یا غیرفعال سازی کلی این پروتکل را دارید.


## فعال‌سازی یا غیرفعال‌سازی پروکسی
 برای این کار از منوی `تنظیمات`، به بخش `پروکسی‌ها` بروید.

<div align=center>

![SSH proxy_proxy](https://github.com/hiddify/hiddify-config/assets/125398461/0c72ddcb-2a4e-4539-af39-2a89f97d89e3)

</div>

در اینجا می‌توانید پروکسی SSH را فعال یا غیرفعال نمایید.


## استفاده از کانفیگ برای اتصال
حالا اگر به صفحه کاربری خود در پنل بروید، می‌بینید که کانفیگ SSH به کانفیگ‌های قبلی اضافه شده است. این کانفیگ به صورت مجزا قابلیت اضافه شدن به نرم‌افزارهای کلاینت را دارد.

<div align=center>

![user link](https://github.com/hiddify/hiddify-config/assets/125398461/1ee96839-715d-4660-afd2-d66f4b3a2f5d)

</div>

برای استفاده از این پروکسی در کلاینت، در حال حاضر می‌بایست از اپ SingBox استفاده نمایید که در این آموزش طریقه استفاده از آن توضیح داده شده است.