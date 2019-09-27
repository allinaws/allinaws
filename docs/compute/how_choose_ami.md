#如何选择AMI镜像

现在AWS软件市场上有的镜像如下：

Windows 2003R2/2008/2008R2/2012/2012R2/2016 

Amazon Linux 

Debian 

Suse 

CentOS 

Red Hat Enterprise Linux 

Ubuntu

##1.快速启动

如下图，建议不选择这个里面AMI来直接跑生产，仅用来测试使用；也可以进行初始化后做一个AMI

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/NKVlcm34T9spMmtxWZ0jb.png)

## 2.我的AMI

这个选项中存放的是你自己定义的AMI

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/DAIm1cHXR10GOGSc4rfjW.png)

##3.AWS Marketplace

AWS商店的AMI优先选择使用，可以直接在搜索框按照名称直接搜索

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/QROV6w2gsz8MX0M9pT1hI.png)

## 4.社区 AMI

此选项内的AMI由个人上传的，也有组织上传的，反正是五花八门的，不是很安全；

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/ADYMOxTjiVpGj8V0LBuc7.png)

## 5.根据需求，进行相关的匹配得到想要的AMI

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/7zbhjFPhg16mPIkuPOXW4.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/a1tVKhOB6BXDYWnaYjTz0.png)

## 6.仅免费套餐

AWS免费提供使用的AMI

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/8R0K6UwSge5nOGysOtsE5.png)

##7.选择AMI注意事项

选择提交人为官方提供的AMI

比如，

AmazonWebServices的 

CentOS就选择Centos.org

Ubuntu选择Canonical Group Limited

这些提交人都是官方的

还有一些第三方提供的，无法保证安全

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/centosami.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/awslinuxami.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_choose_ami/ubuntuami.png)



个人建议 使用一下AMI做实验

CentOS、ubuntu、windowsserver