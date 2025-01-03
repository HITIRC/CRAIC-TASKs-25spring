# Aelos&Roban 选拔任务

## 1 任务要求
#### 1.1 基本任务
***综合使用Linux、python、ROS、OpenCV等，完成简单的图像处理与发布***
1. 对下列图像进行处理，通过python的opencv库函数实现将图像中的红色小球框选并输出其坐标
原图及识别效果图：

<img src="https://ultramarine-image.oss-cn-beijing.aliyuncs.com/img/image-20221027164357622.png" width="300"/>
<img src="https://ultramarine-image.oss-cn-beijing.aliyuncs.com/img/image-20221027164345370.png" width="300"/>

2. 自主编写代码完成以下两个文件 img_pub.py（发布） 与 img_sub.py(订阅)，对[给定图像](https://ultramarine-image.oss-cn-beijing.aliyuncs.com/img/image-20221027164357622.png)进行处理
- img_pub.py文件通过cv_bridge获取摄像头图像并通过ros的publisher发布图像
- img_sub.py文件接收上面的图像话题（topic）， 然后进行图像处理， 结合第一次任务的代码， 还是提取摄像头中的红色物体（自己周围找一个就行，比如苹果之类的，阈值自己摸索调整）， 然后进行框选输出坐标与矩形形状。处理完图像后将新的图像进行发布
- 利用rqt_image工具查看处理完后输出的图像topic

#### 1.2 进阶任务
***使用yolo***
1. 完成一个yolo识别程序，并可以将识别到的某个物体的位置信息发布到ros节点中，

#### 1.3 SLAM任务
***Roban赛道定位算法*** 
- 对于ROBAN赛道的参赛人员，需要学习SLAM的相关知识
- 采用的基本框架为ORB-SLAM2，需要跟随高翔视觉SLAM14讲（b站课程进行学习），至少了解其基本原理
--- 


## 2 参考学习路线
#### 2.1 Python
- 只需要懂Python的基础语法，可以不必学精通，在实践的过程中逐步补全python知识体系，在实践中学习的效率更高效
#### 2.2 Linux
- 学会linux操作系统基础知识，会linux操作系统使用方法
#### 2.3 ROS1
- 教程：[【古月居】古月·ROS入门21讲 | 一学就会的ROS机器人入门教程_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1zt411G7Vn/?spm_id_from=333.337.search-card.all.click&vd_source=7f5cce988a73a29b0bdf6ea667a08dba)
- 理清ROS框架中的命令和功能
#### 2.4 OpenCV
- opencv安装：[windows环境下的Anaconda安装与OpenCV机器视觉环境搭建_iracer的博客-CSDN博客_anaconda opencv安装](https://blog.csdn.net/iracer/article/details/80498732)
- 跟随课程学习，学到27节即可[【2022B站最好的OpenCV课程推荐】OpenCV从入门到实战 全套课程（附带课程课件资料+课件笔记）图像处理|深度学习人工智能计算机视觉python+AI_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1PV411774y/?spm_id_from=333.337.search-card.all.click)
--- 

## 3 补充说明
- 学习目的：熟悉linux系统操作，并能将全流程跑通，不要求对流程中的每一个环节都完全理解，但是先把整个流程跑通，并能展示仿真效果
- 只要跟着视频教程走一定可以跑通，每一步都会在视频教程中有完整说明