# pan-light

```
                     _ _       _     _   
                    | (_)     | |   | |  
 _ __   __ _ _ __   | |_  __ _| |__ | |_ 
| '_ \ / _` | '_ \  | | |/ _` | '_ \| __|
| |_) | (_| | | | | | | | (_| | | | | |_ 
| .__/ \__,_|_| |_| |_|_|\__, |_| |_|\__|
| |                       __/ |          
|_|                      |___/       
                             
```
# pan-light

>　pan-light 是一款不限速的百度网盘客户端, 基于 golang + Qt5 开发.
本项意义在于探究 golang 在图形界面客户端; web 服务端; 事件调度, websocket, p2p 长连接 等方面的应用和实践.
欢迎广大 golang 开发者参与本项目. 

[软件官网](https://pan-light.peterq.cn) | [在线体验](https://pan-light.peterq.cn/demo) | [技术文档](https://pan-light.peterq.cn/doc) | [交流群: 438604465](https://jq.qq.com/?_wv=1027&k=52HpwTS)

## 特性

- 利用golang轻量级协程, 高并发分段下载, 可通过调节并发数达到最佳下载速度; 下载进度状态数据持久化到磁盘, 实现软件重启后可断点续传;
- 客户端本地实现简单代理, 突破百度防盗链, 将网盘视频喂给qt视频播放组件, 从而在线播放视频
- 在线体验: 用户无需下载, 通过网页即可在线体验本软件部分功能; 该系统可应用于其他客户端产品的在线体验; 
- 在线体验原理: 闲置的个人pc, 通过 docker 开启若干个'虚拟机', 虚拟机内安装好了本软件以及vnc服务.
 用户打开网页, 在服务端的调度下, 网页通过 web rtc 和闲置pc建立p2p连接.
 闲置pc将会打通一条用户网页到docker内部'隧道'. 网页连接虚拟机vnc服务进行远程控制

## 关于
本项目是作者第一个完整的go语言实战项目. 希望对于一些找不到好的实战项目的go语言初学者能起到一点帮助, 
欢迎你们阅读项目技术文档, 源码, 并参与到项目开发. 但也正由于作者也是初学者且项目工作量挺大,个人精力有限等一些原因, 在代码严谨方面还有待后续跟进.
比如,你会看到为了网络数据的传递方便, 项目用了大量的`map[string]interface{}`类型, 并且没有做严格类型判断; 有些低频竞争数据的锁也省掉了, 等等; 欢迎大家一起来完善.

## 软件截图
![截图1](https://qiniu-cdn.peterq.cn/pan-light/img/shot_1.png)
   
![截图2](https://qiniu-cdn.peterq.cn/pan-light/img/shot_2.png)
   
![截图3](https://qiniu-cdn.peterq.cn/pan-light/img/shot_3.png)

![截图4](https://qiniu-cdn.peterq.cn/pan-light/img/shot_4.png)

## 其他

- 本项目花费了作者大量的时间和精力, 如果你觉得本项目对你有帮助, 帮忙点个star.

- 作者QQ

![](https://qiniu-cdn.peterq.cn/pan-light/img/author_qq.jpg)
  
    
