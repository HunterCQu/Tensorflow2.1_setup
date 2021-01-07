# Tensorflow2.1_setup

## Overview
！！！本教程基于Windows10 x86 系统，在Anaconda虚拟环境下搭建Tensorflow2.1！！！
如果你有其他需求，可以去底部找参照表去下载对应的版本，切记要版本对应

- 链接里放着我们需要用到所有的东西
https://pan.baidu.com/s/11KojcB2h_3oE5JdoU8UCzw
提取码：a14h
## Getting Started
-  1.安装PyCharm
      首先在网盘的文件中找到Pycharm的安装包（如需其他版本也可去官网https://www.jetbrains.com/pycharm/自行下载）
      选择安装目录，个人建议是D盘
      这里这两个选项记得勾选，其他两个可选或不选（个人建议全选）
      然后等待就行了
-  2.安装Anaconda
      找到Anaconda安装文件
      选择装给谁，我们按推荐来只给当前用户装就行
      安装目录，再次推荐D盘
      最关键的来了，只选第二个，环境变量我们之后自己手动配置就好
      等待安装结束就行了，安装结束后，你的开始菜单里应该是如图所示才对
      配置环境变量，右击我的电脑-->属性-->高级系统设置-->高级-->环境变量-->系统变量，找到Path进行编辑新建两个如图所示的路径（这是我的路径，你自己需要对应你自己的Anaconda安装路径）
      测试环境变量是否配置成功在Dos窗口键入conda --version， 如图显示则配置成功
-  3.在Anaconda中新建虚拟环境
      打开我们安装好的PyCharm，新建一个工程，红框是你期望的项目文件夹存放位置（这里我放桌面做演示），最关键的是黄框，选择到你的Anaconda文件夹下的python.exe如图是我的路径，创建就Ok了
      我们进来了，哈哈哈，别急！！要等所有的包加载完再操作，等红框里的内容消失就可以了
      打开终端如图所示，键入conda create -n tf python==3.7，过程中提示是否执行操作键入y继续
      创建完成，我们现在需要激活一下这个环境，键入conda activate tf，再次键入conda insall tensorflow-gpu==2.1.0（你的电脑支持GPU训练的话）或者conda insall tensorflow==2.1.0
      等待安装完成
-  4.安装Cuda和配置CUDNN（使用GPU需要配置，CPU无需配置）
      找到Cuda安装文件打开选择路径，切记这里只是一个临时路径，安装结束后这个路径下的所有内容会自动删除，所以需要建立一个独立全新的文件夹来作为这一步的路径
      下一步这里推荐选择自定义安装，然后只选择如下图的组件安装就行（当然如果你不嫌占内存也可以选择默认安装全部安装）
      选择路径，三个目录的路径最好一致，方便之后配置环境变量，放在默认的系统下是比较保险的，我自己是放在其他盘啦，这个不太重要看个人喜好
      等待安装结束就行
      接下来需要配置CUDNN，很简单，做三次文件的复制就行，将CUDNN压缩包下的三个文件夹里的文件，分别对应的复制到CUDA文件夹下就可以，如下图所示
      配置Cuda的环境变量，如下图，（这是我的路径，你需要找到你的Cuda安装目录下的这些路径）
      检验配置是否成功，在DOS窗口切换到你的Cuda文件夹中的\extras\demo_suite中
      分别键入bandwidthTest.exe 和 deviceQuery.exe ,如果提示如图PASS那就Ok了

## Tips
Tensorflow和Cuda及CUDNN存在很强的关联关系，所以版本依赖也很强，如果你需要其他版本的Tensorflow这里提供一下版本参照表给你，希望能帮到你，以及Cuda和CUDNN的下载地址（下载CUDNN需要注册一下）
-  Tensorflow官网Windows搭建的一些建议https://www.tensorflow.org/install/source_windows
-  Cuda下载地址https://developer.nvidia.com/cuda-toolkit-archive
-  CUDNN下载地址https://developer.nvidia.com/rdp/cudnn-archive

      
