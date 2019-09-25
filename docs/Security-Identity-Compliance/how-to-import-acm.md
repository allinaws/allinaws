# 如何导入外部证书

## 1.购买或者申请免费的证书

阿里云、七牛云等等

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-import-acm/01.png)

## 2.上传证书

打开EC2的负载均衡

选择相应的ALB

添加侦听器

选择https

端口443

选择目标组

证书类型

上传证书到IAM

证书名称填写申请证书时候的那个域名

私有密钥，填写申请的那个后缀为key的文件直接复制到里面

公有密钥证书，填写后缀为pem文件，直接复制到如下图

点击创建

![](https://awschinawiki.s3.cn-northwest-1.amazonaws.com.cn/docs/how-to-import-acm/02.png)