---
title: 在命令行中运行IDEA
date: 2016-08-11 19:14:48
categories: [Java]
tags: java
---

有时候在Terminal中进入项目的目录了，想要直接打开，应为如果去IDEA里打开的话，还得在找一次目录，这个简直是不能忍啊。所以可以弄个命令行中运行IDEA的方法。

第一个方法是使用Mac上的`open`命令，open命令可以在命令行中打开特定的文件，默认调用系统默认对应的应用，比如你open一个目录默认是用Finder打开的。不过open有一个-a参数，可以指定用什么软件打开，所以可以在你的~/.zshrc中添加：

```
alias idea="open -a /Applications/IntelliJ\ IDEA.app"
```

然后就可以用idea命令打开工程目录了😊

还有一个做法，IDEA可以自动生成对应的命令，点击Tools->Create Command-Line Launcher，IDEA就会建立一个/usr/local/bin/idea的可执行文件，命令行中就可以调用了：

![](/img/java/idea-add-cmd.png)

![](/img/java/idea-add-cmd2.png.png)