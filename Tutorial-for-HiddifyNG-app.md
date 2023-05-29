<div dir="rtl">

[**![Lang_Farsi](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](
https://github.com/hiddify/hiddify-config/wiki/%D8%A2%D9%85%D9%88%D8%B2%D8%B4-%DA%A9%D8%A7%D8%B1-%D8%A8%D8%A7-%D9%86%D8%B1%D9%85%E2%80%8C%D8%A7%D9%81%D8%B2%D8%A7%D8%B1-HiddifyNG)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/hiddify/hiddify-config/wiki/All-tutorials-and-videos"><img width="100" src="https://github.com/hiddify/hiddify-config/assets/125398461/8ac5b906-105c-4b98-acf5-0e12e39e33f6" /></a>

</div>


# Tutorial for HiddifyNG app
This app is the best software for connecting to Xray protocols on Android operating system.
Download and install the software

Enter the `Android` tab in your user panel and open the `HiddifyNG` section.

<div align=center>

<img width=30% src="
https://github.com/hiddify/hiddify-config/assets/125398461/5e2272ae-86e8-487c-8d09-f3866585c436" />
</div>



Click on Direct Download to download the application.

You can also download and install the program directly from [GitHub](https://github.com/hiddify/HiddifyNG/releases) and [Google Play](https://play.google.com/store/apps/details?id=ang.hiddify.com).

## Add config
To do this, in the same section related to the `HiddifyNG` program, click on `Click to Import` to add the configuration to the program.

<div align=center>

<img width=30% src="https://github.com/hiddify/hiddify-config/assets/125398461/adf69d91-570b-4fb0-9266-09d3abdd837f" />
</div>




## Edit profiles

To do this, tap on the section related to the profile to open the section related to their settings.

You can edit the imported profiles or add a new profile.

## Proxy mode settings

The settings of this section determine how the traffic of sites and applications pass through the VPN, which consists of three parts.

#### All
All sites and apps pass through the app.


#### Blocked
Passes detected filtered sites through the app.

#### Not Opened
In addition to the identified filter sites, it also passes through the app the sites whose filtering status is unknown.


## Fragment

Fragment splits the sent packets into some pieces. In this way, SNI is hidden from the GFW and filtering will be bypassed. [more information](https://github.com/hiddify/hiddify-config/wiki/How-the-fragment-works-and-its-usage)

The settings in this section determine how information is transmitted in the form of fragmented packets. The purpose of applying these settings is to create resistance against the filtering system.

#### Default
Applies the fragment defined in the config or proxy link.

#### Random
It splits packets into random chunks.

#### SNI
It splits packets into two pieces.


## Connection mode
The settings in this section determine how to connect to configs.

#### Smart
It will automatically connect to the configuration with the highest speed (lowest ping).

#### Load Balance
It connects to several configs at the same time and traffic is distributed between them. This mode is very useful when the IP related to the configs is not clean. By using this mode and spreading the load on several configs, an acceptable speed would be obtained.

#### Manual
Configs are entered manually. By clicking this button, the app opens another page that shows the list of available configs in which you can choose your desired one.


## Connect to the app
To connect to any of the configs, after selecting, you must click on the connect button to connect.

