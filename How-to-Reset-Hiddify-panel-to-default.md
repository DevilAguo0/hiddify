<div dir="rtl">

[**![Lang_Farsi](https://user-images.githubusercontent.com/125398461/234186932-52f1fa82-52c6-417f-8b37-08fe9250a55f.png) &nbsp;فارسی**](https://github.com/hiddify/hiddify-config/wiki/%D8%B1%DB%8C%D8%B3%D8%AA-%DA%A9%D8%B1%D8%AF%D9%86-%D8%AA%D9%86%D8%B8%DB%8C%D9%85%D8%A7%D8%AA-%D9%BE%D9%86%D9%84-%D9%87%DB%8C%D8%AF%DB%8C%D9%81%D8%A7%DB%8C-%D8%A8%D9%87-%D8%AD%D8%A7%D9%84%D8%AA-%D8%A7%D9%88%D9%84%DB%8C%D9%87)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://github.com/hiddify/hiddify-config/wiki/All-tutorials-and-videos"><img width="100" src="https://github.com/hiddify/hiddify-config/assets/125398461/8ac5b906-105c-4b98-acf5-0e12e39e33f6" /></a>

</div>

# How to Reset Hiddify panel to default
In this article, we are going to teach how to raw the Hiddify panel (complete reset of the panel and database) similar to the initial installation. If you intend to return the Hiddify panel to its initial settings, this tutorial is prepared for you. Follow these steps to the end.

* To begin, first [SSH into your server](https://github.com/hiddify/hiddify-config/wiki/How-to-connect-to-server-via-SSH).
* Then, by using the combination keys `ctrl+c` or selecting the `Cancel` button, close the Hidیify menu to access the terminal (command line environment) of your server.

* If after performing these steps, the Hiddify menu is still displayed to you, type the word `clear` and press enter.

> It should be mentioned here that if you need to backup your panel, make a backup of the settings-backup before proceeding.
* Then enter this command in the terminal of your server to completely delete the current database:

```
rm -rf /opt/hiddify-config/hiddifypanel/hiddifypanel.db
```
* Then open the menu again using the following command:

```
bash /opt/hiddify-config/menu.sh
```

* And select `Reinstall` option from the Hiddify menu and wait for the panel to be reinstalled.
* After finishing, you can access the new panel and configure it using the displayed admin links.

In this method, after the re-installation is finished, the panel will be completely retested and similar to the initial installation.