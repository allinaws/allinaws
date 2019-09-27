#AWS 入门小知识

**首先，你要先注册一个AWS账号**

如果需要申请国内AWS账号，可以联系我们挨踢茶馆帮忙申请，有优惠😯～

如果申请全球的账号也可以有优惠～不过优惠只针对企业用户～

联系方式：support@iteablue.com

**然后，先申请IAM用户再说；**

登录到aws控制台，打开IAM控制台，开启MFA安全认证，保证根用户的安全；

申请一个IAM用户并授权此用户最大权限（AWS架构师第一准则，不要使用根用户登录控制台操作）；

用申请的IAM用户进行所有的操作，根用户在没有必要的情况不要使用，并由专人负责；

**然后，熟悉AWS控制台；**

把控制台上面的服务选项都点一遍，看看各个服务在哪里；方便后期使用的话知道点击哪里；

控制台的左下角可以切换语言，如果英语不好的可以换成中文显示；

**然后，熟悉AWS账单管理；**

切换到账单控制台，查看账单

登录账单控制台，看看账单首选项、付款方式、整合账单、税务设置、订单发票、服务抵扣金额、成本管理等等

这个要认真搞下，因为账号区分全球的和中国区账号。

1.汇款方式（信用卡（外币卡&银联卡）、电汇、）

2.发票问题（中国区可以提供发票、全球区没有发票只有收据）

3.缴费时间点（账单生成时间、最迟缴费时间）

**熟悉AWS服务限制**

通过控制台查看服务的限制，或者通过此链接

https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/ec2-resource-limits.html?icmpid=docs_ec2_console

https://docs.aws.amazon.com/zh_cn/general/latest/gr/aws_service_limits.html

服务限制，会更好的控制对于AWS资源的合理利用，防止有心人有意或无意的无节制的开启资源。

还有就是一些其他不知道的原因，某项服务在某个region不能使用，这些都要知道；防止你们公司业务要上线了。发现那个地区没有想使用的服务；因为你测试的时候使用的region跟上线所在的那个region不一样，而且你也没有提前确认；等等原因。

**熟悉AWS的support中心**

技术支持，服务限制申请提高；

技术支持分为三种，开发人员、商业、企业。

具体收费模式请看链接：https://aws.amazon.com/cn/premiumsupport/plans/

还有一种技术支持，就是安排专门的架构师服务于你们公司的，But你公司必须在AWS消费很多大洋才可以伺候你

当然，也可以通过我们挨踢茶馆进行技术支持，欢迎联系​​：support@iteablue.com

## **玩转AWS服务**

**基础玩法**

EC2、ELB、S3、ElastiCache（redis）、RDS（MySql）

建议你们先熟悉上面几个服务，使用默认选项（默认VPC、安全组）等创建简单的三层服务并测试。

因为几乎迁移到AWS，使用的服务属上面几项最多，当然也是最常用的服务；先熟悉熟悉基本情况，打好基础。

**中级玩法**

<font color=red>**首先！！！全面深入学习VPC**</font>

一定要学明白VPC，因为AWS大多数服务，多AZ、高可用，都是基于VPC网络区分开的。

还有个问题就是，强迫症选手做事情是不会选择默认的选项去做事的。。。

通过自定义VPC，进行网络划分；各个服务做使用的网络不同（公有子网、私有子网），后期扩展。

这样做的好处就是，你可以清楚的了解到你们整个架构的划分、业务划分、网络划分、安全防护、后期如何进行架构扩展，都能清楚的了解到；

通过自定义的VPC网络进行服务创建，先把基础那几项服务玩一遍；再去测试其他的服务。

**高级玩法**

DevOps

ECS、EKS

Serverless

面试AWS职位   - . -

 

## AWS官方资料

中国区

官方网站：https://www.amazonaws.cn/

官方文档：https://www.amazonaws.cn/documentation/

全球区

官方网站：[https://aws.amazon.com](https://aws.amazon.com/)

官方文档：https://docs.aws.amazon.com/index.html

AWS解决方案：https://aws.amazon.com/cn/solutions

AWS知识中心（从客户收集的一些最常见问题和请求）：https://aws.amazon.com/cn/premiumsupport/knowledge-center



