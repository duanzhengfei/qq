# 项目: electron仿客户端QQ简易版

简单讲解electron的起源 --- 学习 -- 从入门到放弃！

------

> * 进度：已完成 -- 简易登录页，简易聊天页
> * 目的：学习electron的开发
> * 技术栈：electron + vue全家桶 + elementUi + frozenui
> * 参考文章：[electron安装](https://juejin.im/post/5a572f26f265da3e513305f6#comment)

------
## 效果图

登录页：
![Image text](https://github.com/yuanxin42/qq/blob/master/img/QQ图片20190712100207.png)


## Electron是什么?

> 这是一个由GitHub的工程师Cheng Zhao（又名zcbenz）发起的开源项目,Electron是一个实时框架，允许您使用HTML5，CSS和JavaScript创建桌面应用程序。

> Chromium和Node本身就是广受欢迎的应用程序平台，它们都被独立用于创建雄心勃勃的应用程序。 Electron将两个平台结合在一起，允许您使用JavaScript构建一个全新的应用程序类。您可以在浏览器中执行任何操作

![Image text](https://github.com/yuanxin42/qq/blob/master/img/QQ图片20190712094509.png)

## 图解：

electron由Node.js+Chromium+Native APIs构成。你可以理解成，它是一个得到了Node.js和基于不同平台的Native APIs加强的Chromium浏览器，可以用来开发跨平台的桌面级应用。

它的开发主要涉及到两个进程的协作——Main（主）进程和Renderer（渲染）进程。简单的理解两个进程的作用：

> *  1.Main进程主要通过Node.js、Chromium和Native APIs来实现一些系统以及底层的操作，比如创建系统级别的菜单，操作剪贴板，创建APP的窗口等。

> *  2.Renderer进程主要通过Chromium来实现APP的图形界面——就是平时我们熟悉的前端开发的部分，不过得到了electron给予的加强，一些Node的模块（比如fs）和一些在Main进程里能用的东西（比如Clipboard）也能在Render进程里使用。

> *  3.Main进程和Renderer进程通过ipcMain和ipcRenderer来进行通信。通过事件监听和事件派发来实现两个进程通信，从而实现Main或者Renderer进程里不能实现的某些功能。





