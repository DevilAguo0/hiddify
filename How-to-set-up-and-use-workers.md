<div dir="rtl">

[**![lang_logo](https://raw.githubusercontent.com/stevenrskelton/flag-icon/master/png/16/country-4x3/ir.png) فارسی**](https://github.com/hiddify/hiddify-config/wiki/%D9%86%D8%AD%D9%88%D9%87-%D8%AA%D9%86%D8%B8%DB%8C%D9%85-%D9%88-%D8%A7%D8%B3%D8%AA%D9%81%D8%A7%D8%AF%D9%87-%D8%A7%D8%B2-%D9%88%D8%B1%DA%A9%D8%B1%D8%B2)

</div>

# How to set up and use workers
## What are workers?

Workers is one of Cloudflare's famous CDN services, which is actually a server-less service, through which programming codes can be executed without the need to configure a server or infrastructure. In fact, this service is a type of cloud computing based on SaaS.

In other words, the working method of Workers is that instead of trying to open your website directly (here Hiddify's panel); You send requests to workers and then workers re-send requests to your domain and server.

![](https://user-images.githubusercontent.com/125398461/224561104-dafc3e89-1c0d-4afc-82eb-cce1cec6933a.png)

The purpose here is to hide the domain behind the workers.

## How to use workers?
To use Workers, you need to have an active domain on Cloudflare.

### Domain and subdomain registration on Cloudflare
Here you need a purchased domain and you need to register it in Cloudflare. If you have any doubts about the domain and how to register it; Read [this article](https://github.com/hiddify/hiddify-config/wiki/Domain-types-and-how-to-register-them).

Log in to your Cloudflare account according to the instructions on how to register a domain.

![221572305-50e819ea-0fa4-4548-8851-aab91b797f57](https://user-images.githubusercontent.com/125398461/224561629-dd0be4b5-9345-43b7-aa81-a3bfaaaf5899.png)

Enter the registered domain and register a new subdomain in the DNS field.

![222444012-2fa4a2c2-ff89-493e-b92c-01a26d7788b7](https://user-images.githubusercontent.com/125398461/224561952-cbb99885-46f7-49e2-874d-f48e5b0c9b0d.png)

> There is no requirement that the proxy is turned on. Workers works with both on and off proxy mode.

![Screenshot_20230312_210420](https://user-images.githubusercontent.com/125398461/224562373-5201f8b6-5d5c-492f-a6b9-9c4366d4f9db.png)

After registering the subdomain, you must create your service Workers.

### Construction of service Workers
Go to the Workers section of your Cloudflare dashboard page.

![Screenshot_20230312_185353](https://user-images.githubusercontent.com/125398461/224562657-f433fff0-d4a1-4fe6-95e0-5f4e17337c3d.png)

Then select `Create a Service` option.

![Screenshot_20230312_211625](https://user-images.githubusercontent.com/125398461/224562813-20dc1a02-8d93-446b-a7d9-d90fbae3cda3.png)

Here you can choose the name of your service workers. Cloudflare itself also suggests a name for you. You can change it but note that this name must be unique.

![Screenshot_20230312_212008](https://user-images.githubusercontent.com/125398461/224563236-dc4c5497-b179-46f4-ae53-9c003d3789d6.png)

`Starter` option should also be on `HTTP handler`. Finally, by selecting `Create service`, your workers service will be created.

After that, you need to click on the `Quick edit` button so that you can put your desired code in the workers.

![Screenshot_20230312_213000](https://user-images.githubusercontent.com/125398461/224563711-3675b1dc-5f50-4c34-94b3-d47f5a00f7c8.png)

On the Edit Workers page, delete the default codes on the left side.

![Screenshot_20230312_214001](https://user-images.githubusercontent.com/125398461/224564027-10fb94b7-770f-4a44-82e6-c414469a72f4.png)

Then put the following code in its place.


```
addEventListener(
   "fetch", event => {
       let url = new URL(event.request.url);
       url.hostname = "sub.yourdomain.com";                        
       url.protocol = "https";
       let request = new Request(url, event.request);
       event.respondWith(
           fetch(request)
       )
   }
)
```

> Be careful:
* In the fourth line, you must put the domain registered in the EVA step for the `url.hostname` value.
That is, for example, you have registered the subdomain `sub.domain.com` in Cloudflare according to the description of the first step; Here you need to put that domain for `url.hostname` value.

![Screenshot_20230312_214705](https://user-images.githubusercontent.com/125398461/224564419-d7c47371-afe2-46f6-8db6-10daf9994d5c.png)

Click the `Save and deploy` button. This step was completed successfully.

On the workers page, copy your workers address without `http`. For example, like this:

![Screenshot_20230314_080208](https://user-images.githubusercontent.com/125398461/224895042-d6a4e78b-f98f-4b9f-b6ad-a733eff3213a.png)

This step was completed successfully. Now you have to register the address of your service workers in Hiddify panel.

### Registration of Workers in Hiddify
Go to the Domains menu and click Create.
![Screenshot_20230312_215936](https://user-images.githubusercontent.com/125398461/224565137-834f8fbb-5d8f-4fd0-bf98-0571fed2e542.png)

Make the settings according to the picture above and save.

Work is finished. A CDN domain with the profile of your workers has been added to your previous domains and you can use its connections.

> Final and important point:
* Workers in the free plan only processes 100,000 requests per day, so this service is useful for those who do not have high traffic on their server.

<div align=center>

![Screenshot_20230312_223018](https://user-images.githubusercontent.com/125398461/224566711-4fcb0e2d-f8c2-4eed-a222-f458cffc6e01.png)

</div>