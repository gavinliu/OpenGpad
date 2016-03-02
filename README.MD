# OpenGpad

这是个基于测试框架([UiAutomator](/2016/01/02/Android-测试框架之-UI-Testing-UI-Automator/))做的一款：使用电脑键盘玩手机游戏的软件。

## 初衷

本职工作是做Android开发，电脑环境为Linux，没有好的娱乐方式，手机也是长时间插在电脑上的，所以就寻思着，用电脑键盘当手柄，控制手机玩游戏，于是就有了这个项目。

## 体验视频

<iframe height=400 width=620 src="http://player.youku.com/embed/XMTQ1NTQ2NTIyMA==" frameborder=0 allowfullscreen></iframe>

## 软件使用

1. 下载
2. 手机链接电脑并打开调试模式
3. 打开PC端程序
4. 选择你的手机
5. 等待PC端安装手机端程序 
6. 在手机端编辑映射规则
7. PC端获取规则
8. 选择规则点击开始
9. enjoy it~

## 原理

PC通过adb命令启动一个``UiAutomator``测试用例，测试用例死循环等待接受指令，接受到指令后，根据指令对手机进行操作，操作手机采取注入屏幕点击事件的方式，这样做的好处是，可以支持所有手机软件。

## 开源

项目分为两个部分

1. [OpenGpad-PyQT](https://github.com/gavinliu/OpenGpad-PyQT)：PC端控制程序

2. [OpenGpad-Android](https://github.com/gavinliu/OpenGpad-Android) ：Android辅助程序 用于编辑映射规则 + UiAutomator测试工程

## 相关技术

PyQt：

[Python - Mac下PyQt5环境搭建](http://gavinliu.cn/2016/01/16/Python-Mac%E4%B8%8BPyQt5%E7%8E%AF%E5%A2%83%E6%90%AD%E5%BB%BA/)

Android：

[Android - adb forward实现PC和App的Socket通讯](http://gavinliu.cn/2016/01/19/Android-adb-forward实现PC和Android的Socket通讯/)
[Android - 测试框架之 UI Testing - UiAutomator](http://gavinliu.cn/2016/01/02/Android-测试框架之-UI-Testing-UI-Automator/)
[Android - 测试框架之 UI Testing - 实现多点触控事件](http://gavinliu.cn/2016/02/23/Android-测试框架之-UI-Testing-实现多点触控事件/)
