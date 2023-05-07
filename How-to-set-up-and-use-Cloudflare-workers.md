<div dir="rtl">

[**![Lang_Farsi](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D9%88-%D8%A7%D8%B3%D8%AA%D9%81%D8%A7%D8%AF%D9%87-%D8%A7%D8%B2-%D9%88%D8%B1%DA%A9%D8%B1%D8%B2)

</div>

# How to set up and use Cloudflare workers
Workers is one of Cloudflare's famous CDN services, which is actually a server-less service, through which programming codes can be executed without the need for server or infrastructure configuration. In fact, this service is a type of cloud computing based on SaaS.

In other words, the working method of Workers is that instead of trying to open your website (here Hidify panel) directly; You send requests to workers and then workers re-send requests to your domain and server.

![](https://user-images.githubusercontent.com/125398461/224561104-dafc3e89-1c0d-4afc-82eb-cce1cec6933a.png)

The purpose here is to hide the domain behind the workers.

## How to use a Workers?