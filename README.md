# clib2d（C++ 2D物理引擎）

在[apollonia](https://github.com/wgtdkp/apollonia)的基础上，结合先前的[C# 2D物理引擎](https://github.com/bajdcc/PhysicsEngine)，从零开始打造一个简单的2D物理引擎。

## 介绍

先前所做C#版本的[PhysicsEngine](https://github.com/bajdcc/PhysicsEngine)代码翻译自JS物理引擎[matter.js](https://github.com/liabru/matter-js)。

本次借鉴OpenGL工程[apollonia](https://github.com/wgtdkp/apollonia)，两者取长补短。

代码为CMake跨平台，需要使用库：

- freeglut
- opengl32
- glu32
- glm（需要将头文件包含到GCC include库中，有坑，后面将自己实现基本功能）

Win7上使用CLion+MinGW编译没有问题，Linux、MacOS系统下暂未尝试，64位系统需要“-m32”编译。

先前立下雄心壮志[制作简单的2D物理引擎（零）](https://www.cnblogs.com/bajdcc/p/5925837.html)，如今在一点点实现中~

----

## 计划

分阶段最小化原则添加代码，功能由简到繁。

文章发表在知乎专栏：[学习C++](https://zhuanlan.zhihu.com/learncpp)。

目录（暂定）：

1. 使用OpenGL搭建基本框架
2. 工厂模式，渲染第一个矩形物体
3. 时钟同步，给物体添加重力
4. 绘制物体的受力及速度向量
5. 给物体添加旋转
6. 求几何凸多边形的重心和转动惯量（刚体的数据结构）
7. 给物体添加线冲量和角冲量
8. **碰撞检测**
    1. SAT方法
    2. 计算压力作用点（仅限两个以下）位置及方向（及绘制）
    3. 实现摩擦力
    4. 碰撞检测的动态更新
9. 关节（铰链）的实现
    1. 关节的数据结构
    2. 关节的受力分析
10. 实现几种基本场景
    1. 金字塔
    2. 方块堆叠
    3. 牛顿摆
    4. 铰链

## 改进

想到的如下优化：

1. 物体休眠，优化碰撞检测
   
## 截图

待续。

## 参考

1. [apollonia](https://github.com/wgtdkp/apollonia)
2. [matter.js](https://github.com/liabru/matter-js)
3. [PhysicsEngine](https://github.com/bajdcc/PhysicsEngine)
4. [OpenGL](https://www.opengl.org/)
5. [GLUT](https://www.opengl.org/resources/libraries/glut/)
6. [Box2D](http://box2d.org/)
7. [Chipmunk2D](https://chipmunk-physics.net/)