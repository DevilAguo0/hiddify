
<div dir="rtl">

[**![persian_lang](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%DA%86%DA%AF%D9%88%D9%86%DA%AF%DB%8C-%DB%8C%D8%A7%D9%81%D8%AA%D9%86-%D8%A2%DB%8C%D9%BE%DB%8C-%D8%AA%D9%85%DB%8C%D8%B2-%DA%A9%D9%84%D8%A7%D8%AF%D9%81%D9%84%D8%B1)
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
Download the program files and first see Mr. Bashsiz's explanation of how to run it in the video below (persian).

[![](https://user-images.githubusercontent.com/125398461/229997889-eaf51d2c-e5e1-4899-aa34-6c2c73375f10.png)](https://www.youtube.com/watch?v=BKLRAHolhvM)

This program has prerequisites that must be installed in advance.
[jq](https://stedolan.github.io/jq/)&nbsp;&nbsp;&nbsp;[git](https://git-scm.com/)&nbsp;&nbsp;&nbsp;[tput](https://command-not-found.com/tput)&nbsp;&nbsp;&nbsp;[bc](https://www.gnu.org/software/bc/)&nbsp;&nbsp;&nbsp;[curl](https://curl.se/download.html)&nbsp;&nbsp;&nbsp;
[parallel](https://www.gnu.org/software/parallel/)


Then first clone it on your system with the following code.
```
git clone https://github.com/MortezaBashsiz/CFScanner.git 
```
Go to the app download folder and run access to it. 
```
cd CFScanner/bash
chmod +x ../bin/*
```
Download the config.real file. 
```
curl -s https://raw.githubusercontent.com/MortezaBashsiz/CFScanner/main/bash/ClientConfig.json -o config.real
```
It is recommended to change the config.real file based on your configuration.
 
![PICTURE](https://user-images.githubusercontent.com/125398461/234565256-4ebeb511-4876-483a-84c5-cb39d62a12ae.png)


If you want to have your own configuration file, save it under a different name that will not change when the script is updated.

#### Run the script
Go to the location of the downloaded script file and then run the script as shown below.

```
bash cfScanner.sh SUBNET DOWN threads tryCount config.real speed custom.subnets
```

![222946688-bcec3d65-7bf1-495a-b1bf-fe517f69f8822](https://user-images.githubusercontent.com/125398461/234751332-e0fa6e6b-5b97-445b-bd50-12c9d603d556.png)


For example:


```
bash cfScanner.sh SUBNET DOWN 8 1 config.real 100 custom.subnets
```
Finally, the test result is placed in the `result` folder, which you can view and use. More information on the program [wiki](https://github.com/MortezaBashsiz/CFScanner/tree/main/bash).

## Run on Windows version
For the Windows version, install it after downloading the app.

![PICTURE](https://user-images.githubusercontent.com/125398461/222939844-0d312508-d15c-4fe8-b3d9-283e44704339.png)

There are some important files and folders that we need to know for running. See the picture below.

![222940073-b4263585-8116-4527-84ea-ec6ab22148ae2](https://user-images.githubusercontent.com/125398461/234599115-60ac8552-23d2-4f10-8734-d999680d884a.png)


The contents of `v2ray-config` folder here is our config for testing.

![222940243-f84e7a8e-45c9-40a8-bc8d-72202ee00fd62](https://user-images.githubusercontent.com/125398461/234599306-eb9a5edb-ca53-4be2-b74b-aeec3d3e2a5f.png)

>config.real file which is the main configuration information.

>The config.json.template file is the config template file.

>In the generated folder, a structure corresponding to our config is created and tested for each cloudflare IP.

>It should be noted that the structure of this test is based on the vmess configuration, but vless and trojan can also be tested with it.

>So complete the config.real file based on a vmess_ws config in your panel.


![222940550-a2739cc8-c282-41ea-b193-9374d0ec29ff2](https://user-images.githubusercontent.com/125398461/234599586-789e2a5c-8813-410c-b4f3-316a0707a1ab.png)


Finally, to start the test, you can specify the simultaneous test of IPs and press the Start Scan button.


![222940595-8d84cbfb-e391-4762-8da5-c8cd0768579b2](https://user-images.githubusercontent.com/125398461/234599700-ce52e975-3177-457f-9dc1-cac597c6d087.png)


In the Fastest IP found section, it shows the fastest available IP based on the lowest delay.

Recommendations:
- Be sure to edit the config.real file based on your server. It is also recommended
- Do not set the number of IP concurrency more than 8 to give a more accurate output.

Sometimes you may open the app and scan, but nothing is displayed; In this case, there are two modes:
>1. Host address or SNI related to the filtered configuration.
>2. You did not enter the configuration information correctly. For this case, you should open one of the structures placed in the generated folder and check whether the information of this structure is the same as your configuration or not.

![PICTURE](https://user-images.githubusercontent.com/125398461/222940830-906481cb-f8dc-4e3a-abf9-61528f844435.png)

To see the new settings of the Windows version, see [this topic](https://github.com/MortezaBashsiz/CFScanner/discussions/210).

### What to do after finding a clean IP?
After finding a clean IP; You can register it with a DNS record without . That is, create a subdomain on Cloudflare. Turn off the proxy and enter the IP.

![PICTURE](https://user-images.githubusercontent.com/125398461/234565984-a2560018-7106-421f-850d-fb9db5687b26.png)

If you need more information about the domain, [click here](https://github.com/hiddify/hiddify-config/wiki/Domain-types-and-how-to-register-them).



Then in the Hiddify panel, you can put it in the CDN domain settings in the `Force to use host field in the CDN configuration`. [More details](https://github.com/hiddify/hiddify-config/wiki/How-to-configure-Hiddify-Panel-properly#cdn-domain)

![Screenshot_20230427_0656192](https://user-images.githubusercontent.com/125398461/234752684-280b90e8-0b00-4106-b744-b06117821b0f.png)
