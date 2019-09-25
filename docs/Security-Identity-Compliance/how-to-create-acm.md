# 如何创建ACM（Certificate Manager）

AWS Certificate Manager 通俗来讲就是 SSL/TLS X.509 证书，详情请看https://docs.aws.amazon.com/zh_cn/acm/latest/userguide/acm-overview.html

## 1.打开ACM控制台

登录AWS ACM https://console.aws.amazon.com/acm/home

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/01.png)

## 2.选择请求公有证书

键入要使用SSL/TLS 证书保护的站点的完全限定域名

 (例如，www.example.com)。使用星号(*) 创建通配符证书以保护同一域中的若干站点。

例如，*example.com www.example.comsite.example.com images.example.com

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/02.png)

## 3.选择验证方法

使用DNS验证比较方便，而且后期续订也方便

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/03.png)

## 4.审核并请求

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/04.png)

## 5.验证

点击在route53中创建记录，就会自动配置到route53中

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/05.png)

## 6.route53控制台查看

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/06.png)

## 7.AWS Certificate Manager控制台查看

如下图，已经显示验证成功

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/07.png)

## 8.ELB进行配置查看

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/08.png)



![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-create-acm/09.png)



