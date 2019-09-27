# AWS控制台界面介绍

**首部栏**

![头部](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/heard.png)

**底部栏**

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/foot.png)

###服务

这里可以看到AWS的所有服务，也可以在搜索栏进行搜索 快速定位服务

可以看到使用服务的历史记录

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/1.png)

### 资源组

通过启动服务时设置的标签进行资源组分类

什么是资源组（https://docs.aws.amazon.com/zh_cn/ARG/latest/userguide/welcome.html）

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/2.png)

1. 资源组使得同时在⼤大量量资源上管理理和⾃自动化任务变得容易易
2. 资源组是同⼀一AWS区域中与查询中提供的条件相匹配并且共享⼀一个或多个标签或标签部分的AWS资源的集合。
3. 您可以在资源组控制台中构建查询，或者将查询作为参数传递给AWS CLI 中的资源组命令
4. 如果您管理理⼤大量量相关资源（如组成应⽤用程序层的EC2 实例例），则可能需要对这些资源⼀一次执⾏行行批量量操作。

批量量操作的示例例包括：

- ​	应⽤用更更新或安全补丁。
- ​	升级应⽤用程序。
- ​	打开或关闭到⽹网络流量量的端⼝口。
- ​	从您的实例例队列列收集特定的⽇日志和监控数据。

## 快捷访问窗口 

点击图中图钉的按钮，可以把常用的服务拖到如图中的位置；

后期直接点击此处就可以快速访问到访问；

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/3.png)

## 用户

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/4.png)

根用户所显示：

我的账号、我的组织、我的服务配额、我的账单控制面板、订单发票、我的安全凭证

我的账号里面保证注册邮箱、用户ID、等个人信息

组织账号

1 AWS Organizations 是⼀一项账户管理理服务，使您能够将多个AWS账户整合到您创建并集中管理理的组织中。

2 AWS Organizations 包含整合账单和账户管理理功能，通过这些功能，您能够更更好地满⾜足企业的预算、安全性和合规性需求。

3 您可以创建成员账户，还可以邀请现有账户加⼊入您的组织。您可以将这些账户分到不不同的组中，然后应⽤用基于策略略的控制。

4 https://docs.aws.amazon.com/zh_cn/organizations/latest/userguide/orgs_introduction.html

账单成本管理理

1 AWS Billing and Cost Management是⼀一项服务，⽤用于⽀支付AWS 账单、监控使⽤用量量和编制成本预算。

2 AWS 将⾃自动向您在注册新的AWS 账户时提供的信⽤用卡收费。费⽤用每个⽉月都会显示在您的信⽤用卡账单上。

3 您可以在Billing and Cost Management控制台中的付款⽅方式⻚页⾯面上查看或更更新信⽤用卡信息并指定供AWS 收取费⽤用的其他信⽤用卡。

4 https://docs.aws.amazon.com/zh_cn/awsaccountbilling/latest/aboutv2/billing-what-is.html

安全凭证

1 ssh key ⽤用户访问密钥

2 开发者使⽤用，配置awscli sdk

3 https://docs.aws.amazon.com/zh_cn/IAM/latest/UserGuide/id_credentials_access-keys.html?icmpid=docs_iam_console

4 git 认证commit git使⽤用http 开发者使⽤用，配置code commit service

5 https://docs.aws.amazon.com/zh_cn/IAM/latest/UserGuide/id_credentials_ssh-keys.html?icmpid=docs_iam_console#ssh

切换⻆角⾊色

1 当您创建⽤用于跨账户访问的⻆角⾊色时，您在拥有⻆角⾊色和资源的账户(信任账户) 和包含⽤用户的账户(可信账户) 之间建⽴立了了信任。

2 为此，可将可信账号指定为该⻆角⾊色的信任策略略中的Principal。

3 这可能会允许可信账户中的任何⽤用户代⼊入该⻆角⾊色。

4 要完成配置，可信账户的管理理员必须为该账户中的特定组或⽤用户提供切换到该⻆角⾊色的权限。

5 请注意，您只能在以IAM ⽤用户身份登录时切换⻆角⾊色。如果您以AWS 账户根⽤用户身份登录，则⽆无法切换⻆角⾊色。

6 https://docs.aws.amazon.com/zh_cn/IAM/latest/UserGuide/id_roles_use_permissions-to-switch.html?icmpid

## 区域

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/5.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/8.png)

1 两种账号：全球账号、中国账号

2 国外账号：如图显示，

3 国内账号：只有两个区域，北北京（2个AZ）和宁夏（3个AZ）

4 AWS 全球基础设施围绕区域和可⽤用区(AZ) 构建。我们提供两种类型的区域：AWS 区域和AWS 本地区域。

5 AWS 区域提供多个（通常3 个）在物理理上独⽴立且隔离的可⽤用区，这些可⽤用区通过延迟低、吞吐量量⾼高且冗余性⾼高的⽹网络连接在⼀一起。

6 通过这些可⽤用区，AWS 客户可以更更加轻松且更更有效地设计和操作应⽤用程序和数据库。

7 与传统的单⼀一数据中⼼心基础设施和多数据中⼼心基础设施相⽐比，

8 这些应⽤用程序和数据库具有⾼高可⽤用性、容错能⼒力力和可扩展性。

9 AWS 本地区域是单⼀一的数据中⼼心区域，旨在补充现有的AWS 区域，客户希望在其中获得该AWS 区域的灾难恢复选项。

10 与所有AWS 区域类似，AWS 本地区域与其他AWS 区域完全隔离。

11 AWS 云在全球20 个地理理区域内运营着61 个可⽤用区。

12 AWS 边缘⽹网络站点：cdn cloudfort

13 AWS 全球基础设施：

14 https://amazonaws-china.com/cn/about-aws/global-infrastructure/

# 支持中心

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/6.png)

⽀支持中⼼心，⽇日常遇到问题，提问case

1 如果没有购买商业⽀支持，只能提两种⼯工单，

2 ⼀一种是账户和账单⽀支持相关的，另⼀一种就是服务限额的增加

论坛，aws技术论坛

⽂文档，aws官⽅方⽂文档

培训，aws官⽅方培训

其他资源

## 语言切换

根据自身需要切换相应的语言

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/console/7.png)