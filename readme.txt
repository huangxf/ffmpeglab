ffmpegʵ�飺

1. ��������ffmpegԴ����(tar.xz��)����ѹ
2. ʹ��MingwShell��Դ������б���(ʵ���Cygwin����������)
./configure
sudo make
3. ����ɹ�������ffmpeg.exe�Ͷ�Ӧ�Ŀ��ļ�
4. ��ʹ��ffmpeg��ĳ������ʱ:
��1����C���Ա��룬������C++
 (2) ע�����ѡ���п��ļ���˳����Ϊ���ļ�֮��Ҳ���໥�����ģ����Բ���������˳�򣬷������᲻ͨ����
 gcc -Wall -ggdb main.c  
 -IE:/ffmpeg-3.2/ffmpeg-3.2/                          ����Ŀ¼
 -LE:/cppcmd/ffmpegvideo/ffmpegvideo/lib              ���ļ�Ŀ¼
 -------------------------���µĿ��ļ��ļ���˳��������������������ɱ������
 -lavformat 
 -lavdevice 
 -lavcodec 
 -lavutil 
 -lswresample 
 -liconv 
 -lws2_32                                             ����֧�ֿ�
 -lswscale 
 -lm -pthread -o test.exe
