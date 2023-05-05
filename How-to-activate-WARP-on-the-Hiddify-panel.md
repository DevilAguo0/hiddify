<div dir="rtl">

[**![Lang_farsi](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%D8%A2%D9%85%D9%88%D8%B2%D8%B4-%D9%81%D8%B9%D8%A7%D9%84%E2%80%8C%D8%B3%D8%A7%D8%B2%DB%8C-%D9%88%D8%A7%D8%B1%D9%BE-%D8%AF%D8%B1-%D9%BE%D9%86%D9%84-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C)
</div>

# How to activate WARP on the Hiddify panel
Many websites, including Google, restrict the access of users through VPN. Because several different connections go from the same IP server to Google's server at the same time, this behavior is similar to cyber malicious behavior, and because of this, the connection is disrupted, and Google gives a 403 error, for example. Other websites do not allow communication and use of the service. Here is one way to solve the problem using Cloudflare's WARP service.

## What is WARP?
Warp is a Cloudflare service that provides secure and encrypted communication over its network. After performing security checks on the target client and making sure there is no malicious behavior, it opens the connection to the Internet. It assigns an IP to that system and communicates through it. In fact, Warp is a tool that hides your server IP from the sites that your users visit. Because the IP of the server is hidden, so access is established.

Warp has several levels of service, the free service of which has a traffic volume limit, and after crossing the limit, access is limited. It is better to use its special service called WARP Plus, which supports high volume. On Hiddify, it is possible to use this version of Warp, which will be explained later on how to activate it.


## Setting up WARP on Hiddify
Go to the panel settings section, in this section you can see the WARP settings. Open it.

<div align=center>

![Warp_settings](https://user-images.githubusercontent.com/125398461/236473988-c194771e-c6c5-4ee2-ade6-4eff2c84db8b.png)


</div>


When you deactivate it, you must give it a WARP Plus code, which there are different bots in Telegram to receive this code. One of them is [this robot](https://t.me/generatewarpplusbot).

### Mode "All"
It passes all traffic through the warp, even the sites that don't have problems pass through the warp.

### Mode "Only blocked and local websites"
Only domectic sites and `google, spotifiy, netflix, openai, ipinfo.io` use Warp.

- Note: If for any reason there is an error in the inserted code, the warp will be disabled. So make sure to use the code correctly. Select and copy the code provided by the bot correctly and place it in the desired field.