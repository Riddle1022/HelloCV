计算机视觉学习项目 - ROS2 & OpenCV开发环境
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

