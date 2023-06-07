<div dir="rtl" markdown="1">

[**![flag_of_Iran](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%DA%A9%D9%86%D8%AA%D8%B1%D9%84-%D9%85%D9%86%D8%A7%D8%A8%D8%B9-%D8%B3%D8%B1%D9%88%D8%B1-%D8%AF%D8%B1-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/hiddify/hiddify-config/wiki/All-tutorials-and-videos"><img width="100" src="https://github.com/hiddify/hiddify-config/assets/125398461/8ac5b906-105c-4b98-acf5-0e12e39e33f6" /></a>
</div>



# How to monitor server resources on Hiddify





## Free up RAM memory
RAM memory is actually a temporary memory whose space is occupied by running services. Part of the memory is occupied by the operating system itself.

The amount of RAM is not directly related to the number of users on the panel. No matter how many users are defined in the panel, a series of services must be running in order for the operating system and peripheral services to work. Therefore, the number of users on the panel does not have a direct and linear relationship with the amount of RAM, but the running services have a direct relationship with the amount of RAM used.

The operating system is always in charge of managing the server's resources, and if the RAM in your server is filled up to 80%, it is a completely normal thing and you should not worry.

> In Linux servers, do not reboot the system to solve the RAM filling problem.

- One of the ways to improve the server's RAM status is to empty the RAM cache. You can empty the cache with this command in the terminal server when you are logged in as the root user.

```
sync && systemctl -w vm.drop_caches=3
```
> Be sure to be root user and then execute this command.