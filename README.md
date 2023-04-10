## Implementation of some Obsidian plug-in Chinese work

[中文版](README_zh.md)请点击此处

### Preface

As we all know, obsidian is a note-taking software, in my opinion one of its biggest advantages is strong customization, almost can be said that a thousand people using obsidian have a thousand different obsidian, the reason why such an operation can be achieved, but also because it has a large number of plug-ins, but it is very troublesome that many languages in obsidian plug-ins are in English, for people like me who are not very good at English, it is simply a nightmare, but there is no way, and because obsidian's plug-in interface cannot be copied, So either take screenshots for translation, or manually type English for translation, and I also plan to change the software, but I still think obsidian is more suitable for me.

One day when I brushed the B station, I brushed a video of a big guy, the video explained how to use the software made by the big guy to localize the obsidian plug-in, which made me very interested, so I successfully obtained this Chinese software from the big guy according to the information given by the big guy, and used this software with excitement, but as I used it for more time, I found that the software given by the big guy still could not meet all my expectations. Because the information in the main .js file of each plugin is different, this software sometimes cannot be recognized completely or unrecognized, but the effort pays off, and I brushed a more stupid method, that is, I made minor modifications to the main .js, so the next step is to record the process of sinicization.

### Procedure

First make sure you can access Obsidian's third-party plugin marketplace and download plugins, or if there's no magic, download a piece of software called [Watt Toolkit](https://steampp.net/steampp.net). After downloading the required plug-ins, you can perform the localization operation. As can be seen from the figure below, it is still not localized, and the interface of the plug-in is still in English.

![obsidian插件汉化之前](https://cdn.jsdelivr.net/gh/qichenxiaoni/Picture-warehouse@main/img/obsidian%E6%8F%92%E4%BB%B6%E6%B1%89%E5%8C%96%E4%B9%8B%E5%89%8D.png)

Don't worry, find the location where you store these plugins, use VSCODE or other software that can open js files and have a search function to open the main .js file, (here I use VSCODE) Here it is recommended to remember to copy and paste a copy before modifying the main .js file, as a backup, because there may be problems in the modification that cause the plugin to fail or do not want to look after localization, so that you can directly use the old version to restore.

The next operation is much simpler, just use the software's built-in search function to find the English on the plug-in page to modify. For example, the above 'Bind tab to table navigation', use the search function to find it in line 23975 of the file, find it and translate it and then copy it back, and so on, you can realize the localization of the plugin.

![修改main.js文件](https://cdn.jsdelivr.net/gh/qichenxiaoni/Picture-warehouse@main/img/%E4%BF%AE%E6%94%B9main.js%E6%96%87%E4%BB%B6.png)

> It should be noted that sometimes you search for keywords, there may be multiple, do not blindly modify, you can see whether there is '.setName' or '.setDesc' and 'name' and other keywords in front, if you use the '+' sign in the middle to connect, remember not to remove the plus sign inside, such as Advanced Tables This plug-in is like this, and sometimes you may find that the text is mixed with code on the way to Chineseization, Do not translate the code, just translate the text in front of the code, and if there is also the code behind, translate it as well.

If you find in the lookup search that the place it is located does not display name, . setName、. setDesc and so on, don't get excited, directly modify, and then restart the obsidian to see if it takes effect or whether it is wrong, if it is wrong, use the recall function directly to withdraw the modification just made.

![Colorful_tag](https://cdn.jsdelivr.net/gh/qichenxiaoni/Picture-warehouse@main/img/Colorful_tag.png)

Finally, a warm reminder, this method is not permanent, that is, if the plugin is updated, the content you have Chinese will be reset, that is, it will change back to English, so we need to remember to save another modified main .js file.

I will also update some of the main .js files of the Chinese plug-in from time to time, please download it yourself if necessary, remember to change the name of the file to main after downloading.js!!!

