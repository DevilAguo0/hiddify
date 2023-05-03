
<div dir="rtl">

[**![flag_of_Iran](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%D8%A2%D9%85%D9%88%D8%B2%D8%B4-%D8%A7%D8%B3%D8%AA%D9%81%D8%A7%D8%AF%D9%87-%D8%A7%D8%B2-Reality-%D8%AF%D8%B1-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C)

</div>

# How to use Reality on Hiddify
Reality is one of the new protocols provided by Xray, which does not have the prerequisites of the previous protocols. This protocol is based on Vless and therefore cannot be used for Vmees or Trojan. On Hiddify, the emphasis is still on simplification, so most of the work is done behind the scenes.

* Very important point: because this protocol is based on TCP, it does not support CDN, so it can only be used in direct or rail modes, and for this reason, it needs a server with a clean IP. If you need information on how to test the server, refer to [this link](https://github.com/hiddify/hiddify-config/wiki/How-to-make-sure-the-server's-IP-or-domain-is-clean).


## Reality setup in settings
To do this, go to the panel settings and enter the Reality settings.
</div>

<div align=center>

![](https://user-images.githubusercontent.com/125398461/235881686-4d6f6ccb-33aa-4113-9913-e6d083cac6ff.png)

</div>

The panel has automatically made the settings for you, but these settings may not work for every network. Therefore, be sure to click the test link to open the protocol test page.

<div align=center>

![](https://user-images.githubusercontent.com/125398461/235881717-dfd7fd6d-2642-4111-9ee8-0adfe8705413.png)


![](https://user-images.githubusercontent.com/125398461/233787191-cd855014-0ab2-4872-bce2-05d1ae705082.png)

</div>

Here the panel shows the test result on different addresses around your server location. Consider the addresses that have the lowest ping time or TCP ping time.

Return to the Reality settings.

## Fallback Domain 
This domain is used when the filtering system is visiting your website, which causes it to redirect to this address. You can put one of the addresses of the review page that had a lower ping time in this field.

## Private Key
This key is used to encrypt the connection and please do not change it.

## Public Key
This key is also used to encrypt the connection between the server and the client, and please do not change it.

## Server Names
The server name used to simulate the destination of your traffic. You can choose one or more sites from the list on the review page. To use multiple sites use `,` .

## Short IDs
This ID is also used for encryption and please do not change it.

Finally, suppose that `www.yahoo.com` is hosted in your data center and have good ping; Complete the settings as below.

<div align=center>

![](https://user-images.githubusercontent.com/125398461/235890716-70034a9d-0a41-4de9-a39b-d5d20c740399.png)
</div>

At the end, press the register button and don't forget to apply the changes.

<div align=center>

![](https://user-images.githubusercontent.com/125398461/235890855-5b159244-1e83-4eaf-97d5-fef455168911.png)
</div>

Yellow messages may be given here, which are the result of checking your completed fields by the server.

* In Reality, in order not to be recognized, it is better that the selected domain is in your data center, and also note that the server name field and the returned domain must be on the same server.
* That is, you cannot set the return domain to `www.yahoo.com`, but the server name is `www.google.com`. But if you put the name of the server as `blog.yahoo.com`, it is ok.

Finally, considering the above, it is better to make the settings so that these messages do not appear, but if you did not receive an error message (red) and only received warning messages (yellow); You can ignore them and move on.


## Enabling or disabling Reality Proxy
For this, go to the proxies menu and view and control Reality proxies in the direct section.


If you still do not receive its connections in the subscription link despite the Reality options being turned on in this section, check the domain settings used for the subscription link. You probably need to tick the direct domain.

- Important note: because this protocol uses a different algorithm, its settings may be different for different networks, so if you see that it does not work for you, first make sure that your IP server is healthy, and then change the return addresses and the server name. to achieve the desired result.

## Why don't I see these configs in the proxy menu despite enabling the reality protocol?
If you still don't see these connections in the configuration list despite activating the Reality protocol in the proxies section, you need to go to the subscription domain settings and add your direct domain to that domain.
</div>

<div align=center>

![](https://user-images.githubusercontent.com/125398461/235891281-fab58684-87ce-419f-913d-9ae40895f8e8.png)

</div>

Suppose your subscription domain is t1.hiddify.com and your direct link is t2.hiddify.com. You need to go to the t1.hiddify.com domain settings and in the display domain configs field; Tick the domain t2.hiddify.com. Now if you open your subscription link on the t1.hiddify.com domain; You will see that there are Reality configs.

