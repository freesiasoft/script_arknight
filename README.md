# script_arknight
<p align="left">
	<img src="https://github.com/vertuer/script_arknight/blob/master/processed/f9c6cbdc6b.jpg" width="250" height="250">
</p>

## 1.简介
  [EXE文件网盘链接6-7](https://pan.baidu.com/s/1oP-e_mdTc9TMgKX_Qowc2w)  
  提取码：64hq  
  自己写的针对windows模拟器的游戏脚本，现在能自动肝活动本和刷主线1-11，可以参考，可以使用源码二次开发。

明日方舟调用库：  
PIL，pywin32-223，opencv-3.4.3  
少女前线调用库：  
多一个pyocr-0.5.3



## 2.基本原理说明：
  利用抓取windows窗口图像，并对图像进行基本识别操作后对模拟器窗口发送虚拟操作指令，由于是在模拟器之外的，因此原理上不会有风险。
缺点是模拟器无法最小化，因windows程序最小化停止重绘窗口，无法抓取到窗体图像。推荐spy++这个工具，可以获取模拟器的句柄和窗体信息，[spy++下载地址](http://pan.baidu.com/s/1skMJUkH)

## 3.脚本功能（针对2019-5-30版本）
  1.活动图GT2-6可以选择  
  2.理智不足可以碎石    （config_ark.py 配置）  
  3.脚本开始位置无要求，可以从不同界面，或者是战斗中等开始脚本  
  4.自适应分辨率，最高支持1080p， 目前测试了720p没有问题  
  5.支持夜神模拟器  
  6.战斗界面若暂停自动继续  
  7.多重检验，不会因卡顿而选错图或者是没有打开代理

## 4.使用说明
  basic_function.py文件为基础的窗体消息函数，如鼠标点击，获取窗体图像等  
  function_ark.py文件为封装好的具体操作函数及类，实现脚本的具体操作  
  config_ark.py文件为配置文件，包含识别图像的映射关系及一些预设置常量  
  globalvar.py存放全局变量  
  test3.py为主文件
  简易界面如下  
  ![=。=](https://github.com/vertuer/script_arknight/blob/master/123.png)  
  1.选择需要刷的关卡  
  2.输入刷的次数，输入999之类的较大数持续刷图知道理智耗尽  
  3.若想碎石，则选择对应碎的数量，脚本将在每次理智耗尽后碎石，请注意最大碎石数量  
  4.若想通过1-11来完成每日，在脚本界面中间的1-11刷图次数下选择对应次数  
  5.点击开始运行脚本，中途可以点击结束来中断
## 5.后续增加功能：
  1.gui  
  2.打包  
  3.自动每日主线任务  
  4.自动基建干员分配  
  5.其余主线，由于增加了1-11后面更新只要更新图库  
  
## 6.更新内容
### （2019-6-6）
  1.界面设计，基本功能满足  
  2.exe打包，真是个大坑
### （2019-6-7）
  1.增加主线1-11，可以选择刷完活动图后再刷固定次数  
