01: 简介与安装


相信大部分人知道的OpenCV都是用C++来开发的，那为什么我推荐使用Python呢？

本教程翻译自OpenCV官方英文教程，我按照使用度和难易度翻译，重新编写了大量原创内容，将不常用和较难的部分写成番外篇，浅显易懂，很easy的辣。每节的源码、图片和练习题答案均可在引用处找到噢(⊙o⊙)

Python照样快！
众所周知，虽然Python语法简洁、编写高效，但相比C/C++运行慢很多。然而Python还有个重要的特性：它是一门胶水语言！Python可以很容易地扩展C/C++。OpenCV-Python就是用Python包装了C++的实现，背后实际就是C++的代码在跑，运行速度非常接近原生。

比如我分别用Python和C++实现读入图片和调整图片的亮度对比度，结果如下：



可以看到某些情况下Python的运行速度甚至好于C++，代码行数也直接少一半多！

另外，图像是矩阵数据，OpenCV-Python原生支持Numpy，相当于Python中的Matlab，为矩阵运算、科学计算提供了极大的便利性。

人工智能浪潮
近些年，人工智能AI相关技术的快速发展大家有目共睹。在编程语言方面，更多人希望的是具备高效开发效率、跨平台、高度扩展性的语言，尤其是一些AI巨头优先推出支持Python语言的深度学习框架，如Facebook的PyTorch、Google的Tensorflow等，可以说Python是名副其实的“网红语言”了。



从TIOBE编程语言排行榜也可以看到，Python发展迅猛，已经逼近C++的份额。这个排行榜每月更新，就不截图了，我编写时的TOP5：Java/C/C++/Python/C#。

人生苦短，我用Python
如果你搞科研用，果断放弃C++（Matlab？出门左拐）
如果你是快速原型开发，验证方案，果断放弃C++
如果你懒的配置OpenCV环境，果断放弃C++
如果你的程序是在支持Python的较高硬件环境下运行，果断放弃C++
如果你担心Python写不了界面，那是你的问题o_o ....
除非你的程序是MFC或已经用C++编写其他模块或是嵌入式设备，那就用C++吧
"人生苦短，我用Python！！！"

安装
本教程编写时使用的相关版本是：OpenCV 4.x，Python 3.x。

opencv-python
只需终端下的一条指令：

pip install opencv-python
Copy to clipboardErrorCopied
pip是Python的包管理器，如果你还没安装Python，强烈推荐安装Anaconda，它包含了大量的科学计算包，不用后期一个个安装。

Anaconda安装
进入Anaconda官网，下载最新版本的安装文件，速度比较慢的话，可以去清华开源镜像站。

Windows版是exe文件，双击直接安装，安装时记得勾选 Add Anaconda to my PATH environment variable，添加到环境变量。
Linux版是sh文件，执行bash Anaconda3-xx.sh，Linux版也会提示添加到环境变量，记得输yes就行。
MAC版是pkg文件，同样直接双击安装即可。
安装测试
Python的版本可以在终端中输入python --version来查看。对于OpenCV，打开Python的开发环境，输入import cv2，运行没有报错说明一切正常。要查看OpenCV的版本，可以：

print(cv2.__version__)
Copy to clipboardErrorCopied
编辑器我习惯用Visual Studio Code，也可以用PyCharm/Atom/Jupyter Notebook(Anaconda自带)。

常见问题
pip识别不了：pip的目录没有添加到环境变量中，添加到用户(或系统)变量的path中。
下载速度很慢：可到此处下载离线版。终端输入pip install 文件名安装。
学习软件
为了便于学习OpenCV，我编写了一款教学软件LearnOpenCVEdu，目前只开发了一部分功能，欢迎Star支持smiley。



经验之谈：虽然我推荐大家使用OpenCV-Python进行图像处理，但想要深入理解OpenCV，C++是必须的，尤其是OpenCV源码！

引用
本节源码
网络资料
OpenCV Docs官方文档
OpenCV源码
官方英文教程: OpenCV-Python Tutorials
LearnOpenCV、LearnOpenCV Github
OpenCV 中文教程
书籍
Programming Computer Vision with Python、中文书
Practical Python and OpenCV
名校视觉研究所/课程
卡内基梅隆大学
多伦多大学