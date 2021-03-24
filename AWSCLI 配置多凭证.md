## AWS CLI 配置多个凭证

默认情况下，AWS CLI 使用 default 配置文件。
你可以通过指定 --profile 选项并指定名称来创建和使用具有不同的凭证和设置的其他命名配置文件

## 配置参数

```
aws configure  # 设置默认凭证
aws configure --profile jp # 设置名称为jp的凭证
AWS Access Key ID [None]: XXXXXXXXXXXXXXXXXX
AWS Secret Access Key [None]: XXXXXXXXXXXXXXXXXX
Default region name [None]: ap-northeast-1
Default output format [None]: json
```

## 通过配置文件查看配置的信息

注意配置文件里面需要加上`cli_pager =`这个参数

对于AWS凭证，你可以直接修改下面两个文件进行添加凭证

```
~/.aws/config
~/.aws/credentials
```

![](https://img2020.cnblogs.com/blog/1043682/202103/1043682-20210323113646680-1902820369.png)

![](https://img2020.cnblogs.com/blog/1043682/202103/1043682-20210323113745947-1216396375.png)

```
aws sts get-caller-identity
aws sts get-caller-identity --profile jp
```

## 查看profile文件所有配置信息

出所有配置文件名称，请使用 `aws configure list-profiles` 命令。
此功能仅适用于 AWS CLI 版本 2

![](https://img2020.cnblogs.com/blog/1043682/202103/1043682-20210323114430683-622643203.png)



