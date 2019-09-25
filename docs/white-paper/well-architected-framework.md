# 良好的框架

- 设计原则

  - 停止猜测您的容量需求
  - 在生产规模下测试系统
  - 降低架构更改的风险
  - 通过自动化来简化架构实验
  - 支持进化式架构

- 4（6）个支柱

  - 框架

  - 卓越运营支柱

  - 安全性支柱

    - 设计原则

      - 在所有层面应用安全性
        不是仅在基础设施的边缘运行安全设备（如防火墙），而是对您的所有资源（例如所有虚拟服务器、负载均衡器和网络子网）使用防火墙和其他安全控制。 
      - 启用可追溯性
        记录并审核针对您的环境的所有操作和更改。 
      - 自动响应安全事件
        ​监控并自动触发对事件推动或条件推动的警报的响应。 
      - 专注于保护您的系统
        利用 AWS 责任共担模型，您可以专注于保护您的应用程序、数据和操作系统，同时让 AWS 提供安全的基础设施和服务。 
      - 自动实施安全最佳实践
        基于软件的安全机制提高了您更加快速、实惠和安全地进行扩展的能力。创建并保存虚拟服务器的自定义基线映像，然后在您启动的每台新服务器上自动使用该映像。创建在模板中定义和管理的完整基础设施。 

    - 数据保护
      Elastic Load Balancing、Amazon Elastic Block Store (EBS)、Amazon Simple Storage Service (S3) 和 Amazon Relational Database Service (RDS) 等服务包含用于保护您的静态数据和传输中的数据的加密功能。AWS Key Management Service (KMS) 使客户能够更轻松地创建和控制用于加密的密钥。 

    - 特权管理
      IAM 使您能够安全地控制对 AWS 服务和资源的访问。Multi-factor authentication (MFA) 在用户名和密码之外再加了一道安全屏障。 

    - 基础设施保护
      Amazon Virtual Private Cloud (VPC) 可让您预置 AWS 云（用于在虚拟网络中启动 AWS 资源）的私有部分和隔离部分。 

    - 探测性控制

      AWS CloudTrail 记录 AWS API 调用，AWS Config 提供您的 AWS 资源和配置的详细库存，Amazon CloudWatch 是针对 AWS 资源的监控服务。 

      - AWS CloudTrail
        一项记录 API 调用的 Web 服务，记录内容包括调用者的身份、调用的时间、源 IP 地址、参数和响应元素。 
      - Amazon CloudWatch
        一项针对 AWS 资源的监控服务，用于记录以下方面：Amazon Elastic Compute Cloud (EC2) CPU、磁盘和网络活动；Amazon Relational Database Service (RDS) 数据库实例；Amazon Elastic Block Store (EBS) 卷等。CloudWatch 提供了对这些指标和其他指标发出警报的功能。 
      - AWS Config
        一项库存和配置历史记录服务，用于提供基础设施中的配置随着时间的推移而变化的相关信息。 
      - Amazon Simple Storage Service
        通过使用 Amazon S3 数据访问审核，客户可配置 Amazon S3 存储桶来记录访问请求的详细信息，包括类型、资源、日期和时间。 
      - Amazon Glacier
        客户可借助保险库锁功能，利用旨在支持可审核长期保留的合规性控制来保留任务关键数据。 

  - 可靠性支柱
    可靠性支柱包含系统从基础设施中断或服务中断恢复、动态获取计算资源以满足需求以及减少中断（如错误配置或暂时性网络问题）的能力。 

  - 性能效率支柱

  - 成本优化支柱