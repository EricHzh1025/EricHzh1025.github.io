---
layout:     post
title:     vue相关 面试问题
subtitle:  
date:       2019-11-28
author:     
header-img: 
catalog: true
tags:
    - < 版本控制 >
typora-root-url: ..
---



# **git  的常见操作**

**github 高级搜索方法 https://blog.csdn.net/csdnnews/article/details/86570635**



**仓库（Repository）仓库用来存放代码，一个项目一个仓库，多个项目多个仓库**



**初始化个人项目信息：**
**$ git config --global user.name ' EricHzh1025'**
**$ git config --global user.email "[erichzh1025@gmail.com](mailto:erichzh1025@gmail.com)"**

**git status 查看当前工作区和仓库的状态git add** 
**git commit -m "描述添加"**
**git rm a1.php**
**git commit -m "描述删除”**

**git config --list 查看配置信息**

**git clone 克隆github仓库文件克隆到本地**
**github pages 仅仅支持静态网页仓库里面只能是.html文件**
**Git commit git commit 主要是将暂存区里的改动给提交到本地的版本库。每次使用git commit 命令我们都会在本地版本库生成一个40位的哈希值，这个哈希值也叫commit-id， commit-id 在版本回退的时候是非常有用的，它相当于一个快照,可以在未来的任何时候通过与git reset的组合命令回到这里。git commit -m ‘message’-m 参数表示可以直接输入后面的“message”，如果不加 -m参数，那么是不能直接输入message的，而是会调用一个编辑器一般是vim来让你输入这个message，message即是我们用来简要说明这次提交的语句。git commit -am ‘message’ -am等同于-a -m-a参数可以将所有已跟踪文件中的执行修改或删除操作的文件都提交到本地仓库，即使它们没有经过git add添加到暂存区，注意: 新加的文件（即没有被git系统管理的文件）是不能被提交到本地仓库的。**
**Git push 在使用git commit命令将修改从暂存区提交到本地版本库后，只剩下最后一步将本地版本库的分支推送到远程服务器上对应的分支了，如果不清楚版本库的构成，可以查看我的另一篇，git 仓库的基本结构。 git push的一般形式为 git push <远程主机名> <本地分支名> <远程分支名> ，例如 git push origin master：refs/for/master ，即是将本地的master分支推送到远程主机origin上的对应master分支， origin 是远程主机名。第一个master是本地分支名，第二个master是远程分支名。git push origin master如果远程分支被省略，如上则表示将本地分支推送到与之存在追踪关系的远程分支（通常两者同名），如果该远程分支不存在，则会被新建git push origin ：refs/for/master如果省略本地分支名，则表示删除指定的远程分支，因为这等同于推送一个空的本地分支到远程分支，等同于 git push origin –delete mastergit push origin如果当前分支与远程分支存在追踪关系，则本地分支和远程分支都可以省略，将当前分支推送到origin主机的对应分支git push如果当前分支只有一个远程分支，那么主it机名都可以省略，形如 git push，可以使用git branch -r ，查看远程的分支名。**

# **git 下载太慢的解决办法**

**1. 在网站 https://www.ipaddress.com/ 分别搜索：**
**[github.global.ssl.fastly.net](http://github.global.ssl.fastly.net/)的ip**
**[github.com](http://github.com/)的ip**

**2.打开hosts文件**
**Windows上的hosts文件路径在C:\Windows\System32\drivers\etc\hosts**
**3. 在hosts文件末尾添加两行(对应上面查到的ip)**
**![img](file:///C:/Users/Eric/AppData/Local/Temp/enhtmlclip/ScreenClip.png)![img](data:image/png;base64,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+ve6ou/l5udnb+1//gEAAOehRK6wGOlKh8T3eOQcvRhJXTGyaIz778dEpBBoJ4/hrSntBP/lw3tHmjxub03ZbmNbvIRmS5iFhcasEsXIAWOL3oqSKxaOVoxsS5HGeL1ripHJcl25s/p2nSWlRX+Ojo/1bjm1U5R0ZUv7O7FzEgAAuCQlcnXFyDtfvajq7/SYu00l5vjFSH/Vx4vqy/e3j/VjzJUeh+xHo5uwDwXEaMK5U4zs3D5znH9V7/9lf7YwiF4lsDEz/r0cvRjpi56FJcpIW1LEipFRcdE7VjEyLi0OKkamV7dE92tO99pkb3PpzpXYMuH5PD23+99RjAAAwKUrkasqRobCYeYWlZQSxUitLUe2vv/qcfZWmkP3I2bnX9H7nzcTxPaLRo9zu0uvL0WWrqMdW/42mfH493LUYqQvRQ74zoqugJjcSpO62uJCipHU41k75VxCZpnwHOrPbcUIAABcnxK5nmKk+7+/HHLrSaliZCp1i83GEfYjbvc2hKG8mEwSU7crLNRNRNdMPpcVEQeOq3bEYqSdiB84nu62mR2pUqR2IcVIdBtzFl8xkilGunNOMQIAANerRK6jGDlSmXCyYqQZb+RLVVfsx/qJ+ahYSE1Ek5PPBVdI7FGKLJ+sZoqRpds9UjFylFKkvzrko7cjzyXMFiPz69y/GGlLl/lipFsuMob8cWtf3/xVRqlzYPdxxQgAAFyvErn8YuSIV1icohiJfedIY9V+dJPI2qJJXl9q7N6u0k5Ug8dyxUH3XLPN2OR1r1KkH8Pc1SLx8ff6Cffseo5QjOQn9+usvrJithjp1pn6jpL++bliZFJudD/XZoqRdvux22jmz9n+KqbdY7v5veB8i7024/O4+VkxAgAAV6lELrwY6f7PLXWhELPyOzrWFSNdGZLQ/y96h+8L6UXHtH4/chP0foIZSk3kt6VCfrltORG7YmT7XNQwsQ0mx73IJHXN+Bu5UiYsdCa2E+zYNgf9erPrylxJkxQUDiOTkiIqVkD0/8vfrfDWmmXFyPaxfh31c00REv7uaJlGpuhZVCr1r+VgWoZNXqvR664YAQCA61UiV/Xlq4fa/4oRWKsrPCJFwtxVHwAAALeqRBQjAcUIJ9NdbRH7otT2FhXFCAAAwFiJKEYCihFOJ3HFSH97SuaWFAAAgFtVIoqRgGKE04p/f0juf7cLAABwy0pEMRJQjAAAAMD5KhHFSEAxAgAAAOerRBQjAcUIAAAAnK8SUYwEFCMAAABwvkpEMRJQjAAAAMD5KhHFCAAAAHARSkQxAgAAAFyEElGMAAAAABehRBQjAAAAwEUoEcUIAAAAcBFK5OTFyO9+/4fozgEAAACk1H1CiZy8GPnjn/4c3UEAAACAlLpPKJGTFyP//Ne/ozsIAAAAkFL3CSVy8mKkzl//9vfoTgIAAACM1T1CqbySYqRO3fTUl8H4zhEAAABgrO4L6t6g1JUifV5ZMSIiIiIiIiIi8qqjGBERERERERGRm41iRERERERERERuNooREREREREREbnZKEZERERERERE5GajGBERERERERGRm41iRERERERERERuNooREREREREREbnZKEZERERERERE5GajGBERERERERGRm41iRERERERERERuNooREREREREREbnZKEZERERERERE5GajGBERERERERGRm41iRERERERERERuNooREREREREREbnZKEZERERERERE5GajGBERERERERGRm41iRERERERERERuNFX1P1+MOqB+OaElAAAAAElFTkSuQmCC)4.保存更新dns**
**Winodws系统的做法：打开CMD，输入ipconfig /flushdns**
**ipconfig中间有空格**

##  **使用代理 需要ssh翻墙**

**设置代理**   

```text
git config --global http.proxy http://127.0.0.1:1080
git config --global https.proxy https://127.0.0.1:1080
```



