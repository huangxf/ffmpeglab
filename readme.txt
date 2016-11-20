ffmpeg实验：

1. 首先下载ffmpeg源代码(tar.xz包)并解压
2. 使用MingwShell对源代码进行编译(实验过Cygwin但是有问题)
./configure
sudo make
3. 编译成功后，生成ffmpeg.exe和对应的库文件
4. 在使用ffmpeg库的程序编译时:
（1）用C语言编译，而不是C++
 (2) 注意编译选项中库文件的顺序。因为库文件之间也是相互依赖的，所以不能随便调换顺序，否则编译会不通过。
 gcc -Wall -ggdb main.c  
 -IE:/ffmpeg-3.2/ffmpeg-3.2/                          包含目录
 -LE:/cppcmd/ffmpegvideo/ffmpegvideo/lib              库文件目录
 -------------------------以下的库文件的加载顺序不能随意调动，否则会造成编译错误
 -lavformat 
 -lavdevice 
 -lavcodec 
 -lavutil 
 -lswresample 
 -liconv 
 -lws2_32                                             网络支持库
 -lswscale 
 -lm -pthread -o test.exe
