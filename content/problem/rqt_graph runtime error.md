# rqt_graph 运行时错误

1. Arch Linux、ROS indigo运行`rosrun rqt_graph rqt_graph`时报错。

	- 错误内容：

			NameError: global name 'dot_parser' is not defined

	- 错误分析：

		pyparsing包太新

	- 解决方法：

		安装pyparsing 1.5.7 ，如果 `sudo pip2 install pyparsing==1.5.7`无法安装pyparsing 1.5.7 ，则下载[pyparsing源码包](https://pypi.python.org/packages/source/p/pyparsing/pyparsing-1.5.7.tar.gz#md5=9be0fcdcc595199c646ab317c1d9a709)，通过 `sudo python2 setup.py install` 安装。