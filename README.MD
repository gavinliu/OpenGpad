# OpenGpad

这是个基于测试框架([UiAutomator](/2016/01/02/Android-测试框架之-UI-Testing-UI-Automator/))做的一款：使用电脑键盘玩手机游戏的软件。

## 初衷

本职工作是做Android开发，电脑环境为Linux Mint，没有好的娱乐方式，手机也是长时间插在电脑上的，所以就寻思着，用电脑键盘当手柄，控制手机玩游戏，于是就有了这个项目。

## 体验视频


## 软件使用

1. [下载-绿色版本](https://github.com/gavinliu/OpenGpad/releases)
2. 手机连接电脑并打开调试模式
3. 打开PC端程序
4. 选择你的手机
5. 等待PC端安装手机端程序
6. 在手机端编辑映射规则
7. PC端获取规则
8. 选择规则点击开始
9. 回到你的游戏界面, enjoy it~

步骤文字看起来有点繁琐, 推荐看体验视频

## 原理

PC通过adb命令启动一个``UiAutomator``测试用例，测试用例死循环等待接受指令，接受到指令后，根据指令对手机进行操作，操作手机采取注入屏幕点击事件的方式，这样做的好处是，可以支持所有手机软件。

## 开源

项目分为两个部分

1. [OpenGpad-PyQT](https://github.com/gavinliu/OpenGpad-PyQT)： PC端控制程序

2. [OpenGpad-Android](https://github.com/gavinliu/OpenGpad-Android)： Android辅助程序,用于编辑映射规则 + UiAutomator程序,用于注入事件

> QT属于现学现卖写的, 代码风格很混乱, 质量不佳, BUG肯定巨多 各路大神轻拍啊...
>
> 从这个项目可以看出基于测试框架能做很多事情, 对于游戏手柄来说, 完全可以搞个arm板+几个按钮 就能自己搞出一个智能手柄了, 还能适配所有游戏.

## TODO

* 实现摇杆事件
* 实现PC端编辑映射规则

## 相关技术

PyQt：

[Python - Mac下PyQt5环境搭建](http://gavinliu.cn/2016/01/16/Python-Mac%E4%B8%8BPyQt5%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA/)

Android：

[Android - adb forward实现PC和App的Socket通讯](http://gavinliu.cn/2016/01/19/Android-adb-forward实现PC和Android的Socket通讯/)   
[Android - 测试框架之 UI Testing - UiAutomator](http://gavinliu.cn/2016/01/02/Android-测试框架之-UI-Testing-UI-Automator/)      
[Android - 测试框架之 UI Testing - 实现多点触控事件](http://gavinliu.cn/2016/02/23/Android-测试框架之-UI-Testing-实现多点触控事件/)
