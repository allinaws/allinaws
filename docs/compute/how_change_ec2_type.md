# 如何变更EC2实例类型

**使用场景：**

EC2实例类型的变更，由小变大，

比如，由2c4g变为 4c8g 

**查看实例状态**

在变更实例时，需要把此实例停止。（stop状态）才能变更

确认变更之前的实例类型

查看变更之后的实例类型

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/change_ec2_type/01.png)

## 停止实例

1、选中需要操作的实例

2、操作、实例状态、停止

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/change_ec2_type/02.png)

如下状态后就可以变更实例类型

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/change_ec2_type/03.png)

## 变更实例类型

1、选择需要操作的实例

2、操作、实例设置、更改实例类型

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/change_ec2_type/04.png)

**由t2.micro 变更为t3.micro**

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/change_ec2_type/05.png)

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/change_ec2_type/06.png)

## 启动实例

启动实例即可，进行系统查看变更后的实例配置信息







