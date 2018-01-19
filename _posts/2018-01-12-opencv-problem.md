---
layout:     post                    # 使用的布局（不需要改）
title:      opencv安装问题解决 # 标题 
subtitle:   make问题 #副标题
date:       2018-01-12              # 时间
author:     wangcheng                      # 作者
header-img: img/post-bg-2015.jpg    #这篇文章标题背景图片
catalog: true                       # 是否归档
tags:                               #标签
    - 工作
---

## opencv安装问题
>makefile

#### 问题1：
'''make all
CXX/LD -o .build_release/examples/cpp_classification/classification.bin
/usr/bin/ld: .build_release/examples/cpp_classification/classification.o: undefined reference to symbol '_ZN2cv6imreadERKNS_6StringEi'
//usr/local/lib/libopencv_imgcodecs.so.3.0: error adding symbols: DSO missing from command line
collect2: error: ld returned 1 exit status
Makefile:565: recipe for target '.build_release/examples/cpp_classification/classification.bin' failed
make: *** [.build_release/examples/cpp_classification/classification.bin] Error 1
'''' 
#### 解决方法：
'''add the opencv_imgcodecs to the MakeFile
It could be that you are using OpenCV version 3. If yes just uncomment the following line in your Makefile.config:
OPENCV_VERSION := 3
'''

作者：wangcheng
