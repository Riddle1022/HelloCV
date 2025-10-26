第一周：计算机视觉学习项目 - ROS2 & OpenCV开发环境
一：简要介绍：基于Ubuntu虚拟机搭建ROS2和Open CV的开发环境，该内容将会记录详细的搭建过程以及实践总结
二：各版本介绍：操作系统：Ubuntu 22.04 LTS
               Open CV版本：4.5.4
               开发工具：VS Code，Vim，Git
三：具体配置方法：
   1：VMware虚拟机创建：
     i:通过分享的镜像下载Ubuntu和VMware，也可以通过VMware官网进行下载，不过需要注册一个Broadcom账号。
     ii：配置虚拟机的基本信息，包括内存，显示器等
   2：安装ROS 2(fishros版)
     i：检查软件更新：sudo apt update（sudo是以管理员身份进行，update是更新）
     ii：然后运用打包好的安装包安装：wget http://fishros.com/install -o fishros && bash fishros（wget开放源代码软件）
     iii：选择一键配置，更换系统源，选用清华镜像
     iv：安装成功并检验
   3：配置Open CV环境
     i：安装Open CV：sudo apt update 
                     sudo apt install build-essential cmake git pkg-config libgtk-3-dev
                     sudo apt install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
                     sudo apt install libxvidcore-dev libx264-dev libjpeg-dev libpng-dev libtiff-dev
                     sudo apt install gfortran openexr libatlas-base-dev opencl-headers
                     sudo apt install python3-dev python3-numpy
                     sudo apt install libopencv-dev python3-opencv
      ii：安装常用扩展（可选）按Ctrl+Shift+X安装扩展
      iii：配置开发环境
      iv：常用配置设置
      v：配置Git集成
      vi：创建项目工作区
      vii：保存工作区设置
三：使用法则：
 1：编写代码： C++开发：进入 C++ 源文件目录cd HelloCV/src/cpp 
                      创建新的 C++ 文件touch my_opencv_node.cpp
 2：编译代码：编译单个 C++ 文件 g++ -std=c++17 src/cpp/my_opencv_node.cpp -o build/my_node
 3：运行：运行编译后的可执行文件./build/my_node 或者作为 ROS2 节点运行ros2 run hello_cv my_cpp_node

 第二周：本周主要学习Docker和CMake，在熟悉虚拟机基本操作的基础上，学习c++等程序语言在虚拟机上的使用
 本周笔记有三：
《Docker笔记》 《CMake的学习和实践笔记》 《实践任务--凯撒密码》
三个笔记以折叠块的方式呈现，使整体看更为简洁
在学习过程中，借助了豆包等学习工具，同时通过观看up主黑马程序员进行学习，同时借助了部分考核说明上的参考资料
在docker笔记中，先写了对Docker的初步理解，后对其核心概念，安装流程，常用命令等进行具体阐释，同时以笔记的形式记录了Dockerfile,但由于某种原因,Docker Hub难以打开，部分内容有所欠缺（如拉取镜像），我将会继续尝试。
在Cmake笔记中，先写对其的理解，同时根据考核要求进行学习，后描述了安装配置流程，源码外构建，多模块项目管理等内容，经过学习，了解到四个必不可少的内容：主程序、头文件、实现以及CMakeLists.txt,同时我也感受到了，虚拟机的基本操作，都是由终端及其它拓展而成的，也加深了“一切皆文件”的理解
在实践任务中，以main.cpp为例，观察要求，可以采用ASCII码来实现，通过输入的内容，将其存储到动态字符串中，然后进行ASCII对应的换算，有个细节需要注意，当字母比较靠后时，需要考虑再从a开始，需要一个对动态字符串中存储的字母的判断
以上是我学习的内容和笔记的思路与小补充，感谢观看哈
本周笔记链接和第一周一样，在视觉文件中

第三周：本周需要学习通过OpenCV，运用c＋＋，来对照片或视频进行最基础的编辑，以及对颜色的识别。本周内容不杂，但是理解实操难度大，时间较为紧凑，导致实践作业的红绿灯出现一些瑕疵，我将通过接下来的几天里尽可能快地补上缺失的内容，望理解哈
本周笔记有二：《OpenCV基础操作》《实践任务--识别红绿灯》
首先先说本周学习的内容以及成果，通过对b站视频内容的观看，在所分的八个章节中，先学会了打开照片，视频，接着将照片变灰，或者提取某一颜色。接着，学会了生成三角形，矩形以及圆形，矩形左上右下两个坐标确定矩形的方式比较重要，通过对三者的结合，使得可以生成新的图标，并为图标配字。然后可以识别并提取颜色以及图形，至此，本周的实践作业所需知识足够。
第一篇笔记分为两大块，第一块是图片视频的读取等操作，第二块是提取颜色和图形，对于关键的程序我用代码块的方式来展示，同时批注改为红色字体，同时配有部分截图。
接着就是实践任务，实践任务由于时间较为紧张，所配的图片不多，部分代码直接复制第一篇中的内容，可能本篇偏理论，我将会尽可能地补上更多的截图
在我看来，本周的内容难度相比于前两周有所提升，同时实现了部分图像识别的功能，同时更深化了我对c假＋的认识，认识了更多的头文件，也理解了using namespace的真正含义
以上是我学习的内容和笔记的思路与小补充，感谢观看哈
本周笔记链接和第一，二周一样，在视觉文件中
