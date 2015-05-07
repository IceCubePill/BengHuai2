#《崩坏学园2》改进版  ReadMe


这是用《崩坏学园2》的素材，使用Unity3D编写的《崩坏学园2》改进版。

##项目需求

Unity版本 > 4.6.3

##技术简介

###界面

- 采用NUGI插件实现界面编写。
- 界面栈存储界面跳转数据。
- 以动态并发载入方式提高载入速度。
- 自制网格插件实现动态界面编排。
- 实现动态滑动界面

###战斗场景

- 采用自编写的通用内存池方式优化GameObject的创建与销毁。
- 战斗地图采用动态生成可视部分，并且在使用完毕后复用到后面需求的地方。
- 使用Spine制作骨骼动画。
- 碰撞机制上锁死部分方向以达到效率优化。

###整体优化

- 采用事件委托机制来处理事件的传输与处理。
- **自制插件从Excel表中读取数据，自动生成C#对象以及自动导入数据生成XML文件。**
- 采用 Protobuf 来规范协议定义。
- 以自制的特殊单例模式来实现可控创建与初始化游戏数据与对象。
- 通过协程等并发方式来减少阻塞导致的卡顿问题。
- 不使用各种类型的Find语句来优化程序性能。

##运行方式

1. 从 Scenes 文件夹下打开 Main Menu 场景
2. 开始运行
3. 点击战斗或装备界面（目前只完成了这两个功能）
4. 在战斗界面中点击左下角第一个地图，开始游戏
5. 游戏中通过左下角的摇杆进行移动，右下角的武器按键进行攻击

注：目前只完成界面部分的战斗和装备模块，战斗中的移动，攻击，受伤模块，其他还在迭代开发中。

##界面截图

![](http://7xiwp6.com1.z0.glb.clouddn.com/场景1.png)
**战斗模式界面**

![](http://7xiwp6.com1.z0.glb.clouddn.com/编辑装备场景.png)
**编辑装备场景**

![](http://7xiwp6.com1.z0.glb.clouddn.com/场景2.png)
**战斗准备场景**

![](http://7xiwp6.com1.z0.glb.clouddn.com/场景3.png)
**战斗场景**
