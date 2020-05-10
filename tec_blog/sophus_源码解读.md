# Sophus源码解读

## 目录
### Sophus库简介
### C++模板元编程
### 李群、李代数数学原理
### Sophus库各模块功能实现讲解
### Sophus库使用教程
### 文献引用

## Sophus库简介

Eigen是google开发的高效线性代数C++求解库，里面提供了大量数值线性代数算法和位姿几何表示库。但是没有提供李代数的操作。在机器人SLAM领域，将旋转矩阵或者欧式变换矩阵转变为李代数，可以将约束性优化问题转化为无约束优化问题，方便问题的求解。  

Sophus是由Strasdat基于Eigen开发的李代数运算C++库。支持常规的SO(2),SO(3),SE(2),SE(3)等李怠速运算。

### Sohups库结构
![Image text](../resourse/image/sophus_源码解读/sophus_tree.PNG)

软件结构：  

![Image text](../resourse/image/sophus_源码解读/软件库架构.PNG)

## C++模板元编程

### 缘由
由于sophus库使用C++模板元编程实现，这部分对于一部分不熟悉的人比较生涩难懂，所以此部分会对库实现中使用的模板元编程技巧和一些C++特性做简要介绍，如果想理解库的具体实现过程，又不熟悉模板元编程，此部分非常重要，如果仅需要知道如何使用这个库，则不需要看此部分。目前这个库使用的是C++11标准。

### decltype特性

C++11标准中，如果函数返回类型为auto 则需要在函数形参后 ->decltype(根据形参输入的函数返回类型)  

C++14中可以省略此用法，直接用auto填充原来的返回值类型位置就可以。具体参考文献【3】条款3  

### 完美转发

### 变参模板，变参函数  

### 模板特例化













## 李群、李代数数学原理

## Sophus库各模块功能实现讲解

## Sophus库使用教程


## 文献引用
1.视觉SLAM十四讲从理论到实践---高翔  
2.State estimation for robotics---Timothy D Barfoot  
3.Effective Mordern C++---Scott Meyers  
4.https://en.cppreference.com/w/  
5.C++11/14高级编程Boost程序库探秘---罗剑锋  
6.





