# ROS环境安装

ROS全称Robot Operating System，是一套灵活的用于编写机器人程序的框架，
其包含了一系列的工具和库等。大疆的OnBoard SDK和Guidance SDK都包含了ROS
的封装包。以下介绍ROS环境的安装，以`Ubuntu 14.04`为例，也推荐使用Ubuntu 14.04。
其他操作系统支持 `OS X`、`Android (NDK)`、`Arch linux`（测试可行）、`Debian Wheezy`
、`OpenEmbedded/Yocto`，建议安装`Indigo`版本的ROS。

1、确认你的Ubuntu中"`restricted`"、"`universe`"和"`multiverse`"这三个仓库已经启用。
**注意！建议使用官方源，虽然速度较慢，但是可以避免许多不必要的错误，如某些依赖错误等**

2 、添加ROS的仓库地址。**注意！此仓库只支持`Ubuntu 13.10`和`Ubuntu 14.04`**

    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

3、添加密钥

    sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net --recv-key 0xB01FA116

4、安装

    sudo apt-get update（首先不要忘记更新本地数据库）
    sudo apt-get install ros-indigo-desktop-full（推荐安装full包）

5、初始化rosdep

    sudo rosdep init
    rosdep update

6、环境设置

让ROS环境变量自动添加到bash中，当每次bash启动时

    echo "source /opt/ros/indigo/setup.bash" >> ~/.bashrc
    source ~/.bashrc

7、安装rosinstall

`rosinstall`是安装ROS程序的命令行程序

    sudo apt-get install python-rosinstall

安装完成！

