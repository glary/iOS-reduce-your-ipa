# App瘦身



## 资源瘦身
 - 删除无用资源（https://github.com/jeffhodnett/Unused 、https://github.com/tinymind/LSUnusedResources/）
   - 重复的图片（图片名字一样、名字不一样但文件一样）
	- 未使用的图片、音频、视频、plist文件等
	- @1x的图片
 - 资源压缩
   - 图片的无损/有损压缩（ImagOptim压缩工具、https://tinypng.com、 UI设计师出图的时候尽量使用8位图，Adobe Photoshop 选择Save For Web选项）
   - 音频压缩（降低采样率，通常情况下44KHZ就够用了）
   - 使用Assets.xcassets来管理图片

## Xcode's Link Map File
 
   - 在Xcode9中设置 LD_ GENERATE_ MAP_ FILE选项为YES就可以在对应路径中看到LinkMap文件，LinkMap文件是Xcode产生可执行文件的同时生成的链接信息，用来描述可执行文件的构造成分，包括代码段（__TEXT）和数据段（__DATA）的分布情况，进而查看可执行文件的占用大小。

   
## 可执行文件瘦身
 - 去除未使用的第三方库
 - 整理重复的第三方库（例：图片浏览器等）
 - 去除未使用的代码（第三方工具simian扫描(http://www.harukizaemon.com/simian/get_it_now.html)，DEAD_CODE_STRIPPING =YES）
   - 未使用的类
   - 未使用的方法/函数
 - 尽量少的使用属性（减少setter和getter）
  
## 按需资源资源
 - 初始资源的延迟加载
 - app资源的延迟加载
 - 不常用资源的远程存储


## 参考链接
[按需资源](https://developer.apple.com/library/content/documentation/FileManagement/Conceptual/On_Demand_Resources_Guide/index.html#//apple_ref/doc/uid/TP40015083-CH2-SW1)

[苹果官网瘦身指引](https://developer.apple.com/library/content/qa/qa1795/_index.html)
 
[iOS微信安装包瘦身](https://mp.weixin.qq.com/s?__biz=MzAwNDY1ODY2OQ==&mid=207986417&idx=1&sn=77ea7d8e4f8ab7b59111e78c86ccfe66&3rd=MzA3MDU4NTYzMw==&scene=6#rd)
![](http://www.zoomfeng.com/images/2016/10/12/4.png)  
