# MT7601U_ForUbuntu14.04LTS64BIT
MT7601U For Ubuntu14.04LTS @64BIT

小米的芯片也是ralink的MT7601U，去官网下载最新linux驱动就可以了。
只是在修改common/rtusb_dev_id.c文件时，请添加小米wifi的pid
{USB_DEVICE(0x2717,0x4106)},/* XiaoMi wifi */
如果你用的是360wifi二代或者小度wifi或者全民wifi，请添加以下PID（PID来自网络，我手头没有前两个）
{USB_DEVICE(0x148f,0x760b)},/* 360 Wifi 2 Gen */
{USB_DEVICE(0x2955,0x1001)},/* Xiao Du Wifi */
{USB_DEVICE(0x2a5f,0x1000)},/* Quan Min Wifi */

割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割割

独行客
duxingkei
qq:277563381@qq.com

添加以上3种方案的驱动在 ubuntu14.04LTS  64BIT 驱动成功！
只当成网卡使用，这年代，wifi路由这么便宜，谁还要用来当AP发射呢？
编译安装方法
make  
make install
~/app-ubuntu/MT7601U$ sudo modprobe mt7601Usta
然后在右上角的网络上点击，就可以看到wifi扫描出的AP了，点击连接即可，你懂得

感谢:
http://www.freemindworld.com/blog/2013/131010_360_wifi_in_linux.shtml
里面提到的编译错误和解决办法
感谢：
http://blog.sina.com.cn/s/blog_4d31f1650101ejlt.html
里面提到的usb设备的ID，支持主流国内所谓的wifi发射
感谢：nfstry/MT7601U
https://github.com/nfstry/MT7601U
提供的原始代码在git上的，虽然我以前也下载了别的，但是都编译失败后放弃删除了。
https://github.com/nfstry/MT7601U.git



