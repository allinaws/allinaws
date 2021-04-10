![](https://img2020.cnblogs.com/blog/1043682/202104/1043682-20210410190417869-1750221841.png)

## Region 区域

independent geographic area （独立的地理区域）

云资源相连形成的一大片地区成为AWS 区域，表示一个特定的地理区域。以AWS的区域来讲，一个区域就是一个大洲或者国家的一部分(比如，西欧、亚太东北地区或美国西部)

它们描述并记录了云资源的地理多样性，并且由多个可用区(AZ)组成。

AWS区域通常有字符串来表示它所在的地理位置；如下

```
➜  ~ aws ec2 describe-regions --all-regions --output table 
---------------------------------------------------------------------------------
|                                DescribeRegions                                |
+-------------------------------------------------------------------------------+
||                                   Regions                                   ||
|+-----------------------------------+-----------------------+-----------------+|
||             Endpoint              |      OptInStatus      |   RegionName    ||
|+-----------------------------------+-----------------------+-----------------+|
||  ec2.af-south-1.amazonaws.com     |  not-opted-in         |  af-south-1     ||
||  ec2.eu-north-1.amazonaws.com     |  opt-in-not-required  |  eu-north-1     ||
||  ec2.ap-south-1.amazonaws.com     |  opt-in-not-required  |  ap-south-1     ||
||  ec2.eu-west-3.amazonaws.com      |  opt-in-not-required  |  eu-west-3      ||
||  ec2.eu-west-2.amazonaws.com      |  opt-in-not-required  |  eu-west-2      ||
||  ec2.eu-south-1.amazonaws.com     |  not-opted-in         |  eu-south-1     ||
||  ec2.eu-west-1.amazonaws.com      |  opt-in-not-required  |  eu-west-1      ||
||  ec2.ap-northeast-3.amazonaws.com |  opt-in-not-required  |  ap-northeast-3 ||
||  ec2.ap-northeast-2.amazonaws.com |  opt-in-not-required  |  ap-northeast-2 ||
||  ec2.me-south-1.amazonaws.com     |  not-opted-in         |  me-south-1     ||
||  ec2.ap-northeast-1.amazonaws.com |  opt-in-not-required  |  ap-northeast-1 ||
||  ec2.sa-east-1.amazonaws.com      |  opt-in-not-required  |  sa-east-1      ||
||  ec2.ca-central-1.amazonaws.com   |  opt-in-not-required  |  ca-central-1   ||
||  ec2.ap-east-1.amazonaws.com      |  opted-in             |  ap-east-1      ||
||  ec2.ap-southeast-1.amazonaws.com |  opt-in-not-required  |  ap-southeast-1 ||
||  ec2.ap-southeast-2.amazonaws.com |  opt-in-not-required  |  ap-southeast-2 ||
||  ec2.eu-central-1.amazonaws.com   |  opt-in-not-required  |  eu-central-1   ||
||  ec2.us-east-1.amazonaws.com      |  opt-in-not-required  |  us-east-1      ||
||  ec2.us-east-2.amazonaws.com      |  opt-in-not-required  |  us-east-2      ||
||  ec2.us-west-1.amazonaws.com      |  opt-in-not-required  |  us-west-1      ||
||  ec2.us-west-2.amazonaws.com      |  opt-in-not-required  |  us-west-2      ||
|+-----------------------------------+-----------------------+-----------------+|
```

## Availability Zone （AZ）可用区 

AWS可用区是AWS区域的子集，表示一个区域指定部分的云资源，但是它们在网络拓扑结构上是彼此隔离的。
AWS可用区描述和记录了云资源在网络拓扑上的多样性。如果两个云资源属于不同的可用区，即使它们属于同一个AWS区域，你仍然可以认为他们属于两个不同的数据中心。
如果两个云资源属于同一个可用区，它们可能会位于同一个数据中心、同一楼层、同一架构、甚至同一台物理服务器上。

AWS可用区用一个字符串来命名，以该可用区所在的AWS区域名称开始，随后是一个字母。如下
```
➜  ~ aws ec2 describe-availability-zones --output table --region ap-northeast-1
-------------------------------------------------
|           DescribeAvailabilityZones           |
+-----------------------------------------------+
||              AvailabilityZones              ||
|+---------------------+-----------------------+|
||  GroupName          |  ap-northeast-1       ||
||  NetworkBorderGroup |  ap-northeast-1       ||
||  OptInStatus        |  opt-in-not-required  ||
||  RegionName         |  ap-northeast-1       ||
||  State              |  available            ||
||  ZoneId             |  apne1-az4            ||
||  ZoneName           |  ap-northeast-1a      ||
||  ZoneType           |  availability-zone    ||
|+---------------------+-----------------------+|
||              AvailabilityZones              ||
|+---------------------+-----------------------+|
||  GroupName          |  ap-northeast-1       ||
||  NetworkBorderGroup |  ap-northeast-1       ||
||  OptInStatus        |  opt-in-not-required  ||
||  RegionName         |  ap-northeast-1       ||
||  State              |  available            ||
||  ZoneId             |  apne1-az1            ||
||  ZoneName           |  ap-northeast-1c      ||
||  ZoneType           |  availability-zone    ||
|+---------------------+-----------------------+|
||              AvailabilityZones              ||
|+---------------------+-----------------------+|
||  GroupName          |  ap-northeast-1       ||
||  NetworkBorderGroup |  ap-northeast-1       ||
||  OptInStatus        |  opt-in-not-required  ||
||  RegionName         |  ap-northeast-1       ||
||  State              |  available            ||
||  ZoneId             |  apne1-az2            ||
||  ZoneName           |  ap-northeast-1d      ||
||  ZoneType           |  availability-zone    ||
|+---------------------+-----------------------+|
```

注意：
数据中心，这个术语并不在AWS的术语表中，但是为了能够将传统的非云技术与AWS术语对应起来，我们在这里仍然使用它
数据中心是一个用来放置系统资源(服务器)的指定楼层、建筑或者建筑群
AZ包含2+以上的数据中心；

## 置放组

每个数据中心下面还有更小的"单位"：
它们在础硬件上以最大限度减少相关的故障，距离更近一步。
建议将集群置放群组用于可受益于低网络延迟和/或高网络吞吐量的应用程序。
如果大部分网络流量在组中的实例之间进行，也建议使用集群置放群组。要为置放群组提供最低延迟和最高每秒数据包数的网络性能，请选择支持增强联网的实例类型。

详情请看 [https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/placement-groups.html](https://docs.aws.amazon.com/zh_cn/AWSEC2/latest/UserGuide/placement-groups.html)

## 总体架构

上图从整体上展示了AWS云服务的架构。AWS由多个AWS区域组成，为了给全世界绝大数的地方提供高质量的网络访问，这些AWS区域在地理上分布于全球的各个地方。每个AWS区域不仅接入互联网，并且区域之间可以彼此互通，但是同其他互联网一样，它们也需要使用远程网络连接。

一个AWS区域由2+以上的AWS可用区组成。
同一个AWS区域内的可用区之间，通过高速的光纤网络互通，这样访问同一AWS区域内任意两台服务器的速度几乎一样；无须担心它们所处的可用区位置。

一个可用区是由一个或多个数据中心组成，取决于这个可用区的大小。

网络设计使得同一区域内的应用程序可以很容易地部署在多个不同的可用区中，这种分布式设计是为了应用服务可以做“**高可用*，同时保留独立组件之间高速、透明的通信能力，而不用关心他们处于哪个可用区内。

由于AWS区域的设计，整个应用程序必须位于某个区域中，无法做到与其他区域的高速通信。如果你想在多个区域中运行某个应用程序，那么每个区域都需要能够独立运行一台该程序。这样，每个地理区域都可用在本地访问此服务，避免了远程网络通信的代价。

AWS网络流量成本模型，它规定同一区域内的两个可用区之间的通信时免费的，但是跨区域通信或者从区域内访问互联网时需要收取一定的费用

两个区域部署同一套应用程序，这种架构模式不管从成本的角度，还是从时间延迟(区域之间的网络延迟要高于可用区之间的网络延迟)的角度来说，都非常重要。
此外，这种架构可以让应用程序支持各国不同的法规，例如欧盟-美国隐私保护和GDPR

此外，跨AZ有一定的抗灾能力，但显然低于跨Region的抗灾能力。

如果业务想要在多个Region间完整地同步运行，通常需要非常复杂的程序设计，部署上也很麻烦，还容易出现一些数据问题。
大部分跨Region的应用，都是在一个主Region内提供服务，在副Region中同步数据；当主Region挂掉时，人工切换到副Region。这种切换过程用时远远超过跨AZ高可用的恢复用时，而且还可能导致一些没来得及同步的数据损失。这称为“灾难恢复”，跨Region难以实现完全的高可用。

## 可用区不是数据中心

在一个AWS账户中，你基本可以认为两个不同可用区（例如，us-ease-1a和us-ease-1b）中的EC2计算实例，分别位于两个不同的数据中心中。
但是，当你使用多个AWS账户时就不一定了。如果你使用账户1在可用区us-ease-1a中创建了一个EC2实例，同时使用账户2在可用区us-ease-1a中创建了另一个EC2实例，实际上，这两个实例可能就位于不同的数据中心。
为什么会这样？这是因为可用区名称并不是静态映射到指定数据中心的，两个不同的账户，相同的可用区名（例如，us-ease-1a）可能代表了两个不同的数据中心。当你创建一个AWS账户时，它会随机地创建一个可用区到指定数据中心的映射，这意味着虽然都是“us-ease-1a”可用区，但是它们的物理位置可能相隔甚远。

如下图

<table>
    <tr>
        <td ><center><img src="https://img2020.cnblogs.com/blog/1043682/202104/1043682-20210410173340137-1223810234.png" >
        <center>账号A<center>
        </center></td>
        <td ><center><img src="https://img2020.cnblogs.com/blog/1043682/202104/1043682-20210410173354081-1777857674.png" >
        <center>账号B<center>
        </center></td>
    </tr>
</table>

从上图可以看出，一个账户的一个可用区，实际上可能位于多个数据中心中。
这意味着，你在同一个账户、同一个可用区内创建的两个EC2实例，有可能位于同一台物理服务器上，也有可能位于完全不同的数据中心中。
其次，在不同账户中创建的两个EC2实例，即使它们的可用区不同，也不能确定它们是否位于一个数据中心。

> 你需要牢记这一点，原因很简单，即使你在两个不同账户的不同可用区中创建了两个EC2实例，并不代表它们是互相独立的，也不能因此作为高可用的依据。

很多公司会为不同的部门或者群组创建多个AWS账户，而AWS这么做可能是出于计费、权限管理或者其他原因的考虑;有时安全策略要求使用多个AWS账户。

> 当AWS宣布出故障时，它会在其服务状态网站上公布这次故障。但是，当它讨论故障发生在何处时，它会说中断影响了指定区域的“某些可用区”，但不会说具体哪些可用性区受到了影响。

> 这样做的原因是由于AWS的可用区的映射关系：如果我们假设4号数据中心有问题，对你来说可能是“us-ease-1a”，而对其他人来说可能就是“us-ease-1c”。它们无法给出具体的可用区名，因为每个账户下的可用区名都是不一样的。

为什么AWS使用这种怪异的映射方法呢？

主要原因在于负载均衡。当用户要启动多个EC2实例的时候，如果这些实例平均分布在多个可用区中，那么排在后面的可用区可能就没人去关心了。实际上，相比起“us-east-1e”，人们更愿意使用“us-ease-1a”作为常用的可用区名。
这主要还是由人所决定的。如果AWS不采用这种人工映射的方式，按照字母表顺序，字母靠前的可用区就会使用过多，而字母靠后的可用区就会使用较少。通过这种人工映射的方式，AWS可以更有效地来平衡系统压力。

## 如何通过地理多样性真正做到高可用

- 备份在不同的账户中，确保你在每个账户内的多个可用区中都保留了备份;不要跨账户来比较可用区。
- 本地备份

> 作为欧盟安全港的继承者，欧盟-美国隐私保护计划是一套隐私保护原则，用来管理欧盟公民对欧盟以外国家的数据传输行为。它通常关心的是如何存储数据才能符合当地的法律，而AWS区域的概念正是为此提供了支持。
> GDPR，或者称为一般数据保护条例（General Data ProtectionRegulation），规定了欧盟公民的数据必须如何处理。

## 参考资料：

AWS官方文档
可伸缩架构：云环境下的高可用与风险管理