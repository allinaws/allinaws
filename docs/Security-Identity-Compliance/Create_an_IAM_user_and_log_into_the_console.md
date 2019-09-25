#创建IAM用户并登录控制台

##1.登录AWS控制台，打开AMI控制台、点击用户、添加用户

![image-20190910152838584](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/mA4QW880hXSI1hBiMus5n.png)

## 2.设置用户名、访问类型

选择访问类型：

如果是控制台管理人员就选择aws管理控制台访问

如果是开发人员选择编程访问

控制台密码，选择自动生成，并勾选下面需要重置密码的选择

![image-20190910152934320](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/mUSU6TQz31WHjarawUnwj.png)





## 3.设置权限

选择直接附加现有策略，选择搜索AdministratorAccess

![image-20190910153017412](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/8xrHD2mS0HNIREB2lF6sh.png)

## 4.标签这里可以默认忽略



![image-20190910153045604](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/bUsFcJGW5KVZFLJfndPPa.png)

##5.review一下，查看没有问题后点击创建用户

![image-20190910153122268](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/G8qDK7WtOvrfWGivtWtZ0.png)



##6.查看登录地址

![image-20190910153138498](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/7uxzzC27ZWHwybux5BA00.png)



## 7.使用IAM用户登陆

账号ID

用户名

密码

IAM用户登陆地址

https://account-id-or-alias.signin.aws.amazon.com/console

<img src="https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/avag4OIEKiwENfEuxnPbh.png" alt="image-20190910153213685" style="zoom:50%;" />



##8.控制台登录

密码策略第一次登录需要修改密码

![image-20190910153236172](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/compute/article001/Y47PCFviiO7KqVPknQlQQ.png)