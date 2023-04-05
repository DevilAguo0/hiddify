
<div dir="rtl">

[**![lang_logo](https://raw.githubusercontent.com/stevenrskelton/flag-icon/master/png/16/country-4x3/ir.png) فارسی**](https://github.com/hiddify/hiddify-config/wiki/%DA%86%DA%AF%D9%88%D9%86%DA%AF%DB%8C-%DB%8C%D8%A7%D9%81%D8%AA%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%D8%AA%D9%85%DB%8C%D8%B2-%DA%A9%D9%84%D8%A7%D8%AF%D9%81%D9%84%D8%B1)
</div>

# Guide for finding a clean Cloudflare IP
The largest CDN service provider in the world is Cloudflare, and you probably know; Due to the severe filtering of the Internet in Iran, there is a lot of disruption to its services because it is not possible for the filter to completely filter it, but it can cause disruption.
Here, if you also use CDN Cloudflare services; You will be affected by these disorders. To reduce the impact of these disturbances, you should find clean IPs (IPs that are not disturbed).

Here are some ways of working for this issue. 

Tip:
Before starting, it is emphasized that all these tests must be done on the client system without connecting to VPN.

## Using the script of Mr. Morteza Bashsiz
Mr. Bashsiz is an Iranian engineer who has developed a program called CFScanner, which can be used to test the list of Cloudflare IPs on different networks and reach the clean Cloudflare IPs.

This program is published in two versions, Linux and Windows. To do this, first download the desired version from here and then follow how to run it based on the desired operating system.


### Run on Linux version
Download the program files and first see Mr. Bashsiz's explanation of how to run it in the video below. 

[![](https://user-images.githubusercontent.com/125398461/229997889-eaf51d2c-e5e1-4899-aa34-6c2c73375f10.png)](https://www.youtube.com/watch?v=BKLRAHolhvM)

This program has prerequisites that must be installed in advance.
[jq](https://stedolan.github.io/jq/)&nbsp;&nbsp;&nbsp;[git](https://git-scm.com/)&nbsp;&nbsp;&nbsp;[tput](https://command-not-found.com/tput)&nbsp;&nbsp;&nbsp;[bc](https://www.gnu.org/software/bc/)&nbsp;&nbsp;&nbsp;[curl](https://curl.se/download.html)&nbsp;&nbsp;&nbsp;
[parallel](https://www.gnu.org/software/parallel/)


Then first clone it on your system with the following code.
```
git clone https://github.com/MortezaBashsiz/CFScanner.git 
```
