# 如何启动一个EC2

注：这里使用的是默认VPC启动的

## 打开EC2控制台

点击启动就是开始创建EC2实例，AWS没有创建的字眼，启动就是创建；

<img src="https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/01.png" style="zoom:48%;" />



## 选择AMI 

根据自身需要或者业务上面的需要，进行选择镜像；也可以查看[**如何选择AMI**](https://awschina.wiki/docs/compute/how_choose_ami.html)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/02.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/03.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/04.png)

## 选择实例类型

根据业务需求，选择实例类型，AWS没有自定义配置的选择实例。只能通过控制台上面显示的进行选择。

查看官方文档实例类型说明

https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/instance-types.html

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/05.png)

## 实例配置详情

！！这里是最重要的，我们是测试dome这边全部默认，不选择

注意：实例的数量、网络、子网、自动分配公有IP、IAM角色、启用终止保护等后面会细讲；

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/07.png)

## 添加存储

系统盘和数据盘的选择；默认是8G

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/08.png)

## 添加标签

标签分类，对于后期管理服务器很防备

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/09.png)

## 配置安全组

可以选择新建或选择现有的安全组

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/11.png)

## 核查实例启动

检查刚才选择的配置，是不是你所需要的。

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/12.png)

## 选择密钥

！！注册 这里一定要确保你的密钥在你手上，如果没有的话，无法再次找回。（也不是那么绝对，但是太麻烦，几乎不能找回）

创建新的密钥对，创建后一定要下载密钥对到本地电脑上；

选择其他密钥，确保你选择的密钥对在你电脑上或者其他同事电脑上；

选择好密钥对后，并保证本地PC有密钥，可以点击启动实例了。

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/13.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/14.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/15.png)

## 控制台查看启动的实例

了解EC2控制台实例信息

Name、实例ID、实例类型、可用区、实例状态、状态检查、警报、公有DNS、公有IP等、

安全组、AMIID、VPC、私有子网、网络接口等信息

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/how_launch_ec2/16.png)





