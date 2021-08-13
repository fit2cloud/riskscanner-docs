# 更新日志

v1.4.1
------------------------
2021年08月13日

!!! summary "🚀 性能优化 Optimization"
- feat（扫描规则）：优化阿里云、华为云 ram、iam等无区域资源扫描，防止每个区域都扫描一遍数据重复。
- feat（扫描规则）：优化阿里云、华为云、腾讯云区域资源过多的分页查询问题。
- fix（扫描日志）：解决扫描结果日志页面，点击扫描日志/扫描API/扫描结果等按钮演出二级页面报错的问题。
- fix（云账号）：解决 AWS 国际区账号有代理的时候，获取不到区域的问题。

v1.4.0
------------------------
2021年07月27日

!!! info "🌱 新功能 Features"
    - feat（规则引擎）：新增 Nuclei 规则引擎，Nuclei 是 github 上基于 YAML 模板的网络侦查安全漏洞扫描的开源项目。
    - feat（云平台）：集成 Nuclei 到 Riskscanner, 将 Nuclei 当做 Riskscanner 里的一个无校验的云账号，只许输入目标地址，即可应用 Nuclei 无账号扫描。
    - feat（扫描规则）：新增 Nuclei 内置规则示例，可自行添加 nuclei-templates 或自己编写的 yaml 进行扫描。
    - feat（扫描日志）：新增扫描日志查看，包括扫描日志、扫描API、扫描结果。

!!! summary "🚀 性能优化 Optimization"
    - feat（actions）：优化 workflows 打包的 actions。
    - feat（文档docs）：优化 riskscanner.io 官网文档内容与格式样式。
    - feat（扫描结果）：优化 Nuclei 扫描结果信息。

!!! success "🐛 Bug修复 Bug Fixes"
    - fix（腾讯云）：修复CVM实例公网IP扫描未绑定IP时报错的问题。
    - fix（代码安全漏洞）：解决riskscanner代码质量扫描一处SQL注入漏洞的问题。
    - fix（基础镜像）：修改custodian基础镜像的镜像源。
    - fix（install）：修复数据库初始化报错的问题。

v1.3.2
------------------------
2021年07月14日

!!! summary "🚀 性能优化 Optimization"
    - feat（扫描规则）：新增用户自定义阿里云监控扫描规则，详情请访问https://docs.riskscanner.io/question/rule 和 https://docs.riskscanner.io/question/example。
    - feat（login）：优化当login页面输入密码错误提示弹框不合理的问题。
    - feat（策略）：优化腾讯云 IAM 策略信息。

v1.3.1
------------------------
2021年07月02日

!!! summary "🚀 性能优化 Optimization"
    - feat（install脚本）：修正 mysql 持久化配置文件。
    - feat（定时任务）：优化删除扫描结果后，定时任务无法执行的问题。
    - fix（规则组）：修复点击规则组查看扫描规则分页无效的问题。
    - fix（定时任务）：解决定时任务选择云账号提示未选择的问题。


v1.3.0
------------------------
2021年06月30日

!!! info "🌱 新功能 Features"
    - feat（云账号）：新增 Google Cloud 云平台，内置扫描规则、规则组，支持平台资源的扫描。
    - feat（定时任务）：新增定时任务详情页面，展示定时扫描的云账号规则等信息。
    - feat（扫描规则）：新增vpc相关的阿里云内置规则。

!!! summary "🚀 性能优化 Optimization"
    - feat（install脚本）：优化 riskscanner 的安装打包方案，在线包与离线包采用全新的zip安装方式，详情请看 riskscanner.io 官网。
    - feat（文档docs）：优化 riskscanner.io 官网文档内容与格式样式。
    - feat（定时任务）：优化定时任务日志信息。
    - feat（云账号）：优化 Google Cloud 云平台 IAM 策略信息。

!!! success "🐛 Bug修复 Bug Fixes"
    - fix（一键扫描）：修复一键批量扫描，因已保存区域数据而报错的问题。
    - fix（云账号）：解决 定式任务状态不准确的问题。
    - fix（扫描规则）：修复腾讯云、华为云安全组扫描结果不准确的问题。
    - fix（扫描规则）：修复阿里云RDS公网扫描结果不准确的问题。


v1.2.1
------------------------
2021年06月17日

!!! info "🌱 新功能 Features"
    - feat（云账号）: 新增定时任务功能（定时扫描某些云账号或某些规则）。
    - feat（API）: 新增 RiskScanner Restful APIs 测试用例。

!!! summary "🚀 性能优化 Optimization"
    - feat（扫描规则）: 优化各个云平台安全组的规则，比如规则似乎是将条件解释为OR而不是AND。优化VMware vSphere VM/ResourcePool 扫描规则。
    - feat（扫描结果）: 优化后端性能，提升扫描速度，降低扫描时间。
    - feat（云账号）: 优化云账号校验，无效状态校验提示失败。

!!! success "🐛 Bug修复 Bug Fixes"
    - fix（云账号）: 解决 Azure 国际区账户验证失败的问题。
    - fix（扫描结果）: 解决扫描结果按规则组维度显示的问题。
    - fix（云账号）: 解决 IAM 策略信息的导入云平台报错问题。
    - fix（云账号）: 解决 Azure 国际区账户验证失败的问题。


v1.2.0
------------------------
2021年05月26日

!!! info "🌱 新功能 Features"
    - feat（云账号）: 新增 OpenStack 私有云平台，内置扫描规则、规则组，支持平台资源的扫描。
    - feat（云账号）: 新增 VMware vSphere 私有云平台，内置扫描规则、规则组，支持平台资源的扫描。
    - feat（扫描结果）: 新增安全合规报告下载功能。

!!! summary "🚀 性能优化 Optimization"
    - feat（云账号）: 优化 aws、azure、aliyun、huawei、tencent 等平台 IAM 策略信息。
    - feat（扫描规则）: 优化规则组与规则的显示，点击规则组显示对应的规则列表。
    - feat（云账号）: 新增 VMware vSphere 私有云平台，内置扫描规则、规则组，支持平台资源的扫描。

!!! success "🐛 Bug修复 Bug Fixes"
    - fix（扫描结果）: 解决优化改进建议不正确的问题。
    - fix（扫描结果）: 解决扫描结果按规则组维度显示的问题。
    - fix（云账号）: 解决 IAM 策略信息的导入云平台报错问题。
    - fix（云账号）: 解决一键扫描未扫描已保存的参数的问题。


v1.1.1
------------------------
2021年04月29日

!!! success "🐛 Bug修复 Bug Fixes"
    - fix: 解决登录页面报错，弹框认证信息已过期的问题。


v1.1.0
------------------------
2021年04月27日

!!! info "🌱 新功能 Features"
    - feat（云账号）：新增 Amazon Web Services 云平台，内置扫描规则、规则组，支持 AWS 国际区、中国区平台资源的扫描。
    - feat（云账号）：新增 Microsoft Azure 云平台，内置扫描规则、规则组，支持 Azure 中国区、国际区、美国区、德国区平台资源的扫描。
    - feat（代理）：新增 http/https 代理配置，云账号绑定并启用代理。
    - feat（通知）：新增消息通知类型，钉钉通知。
    - feat（通知）：新增消息通知类型，企业微信通知。

!!! summary "🚀 性能优化 Optimization"
    - feat（云账号）：优化添加云账号，可批量添加云账号。
    - feat（云账号）：优化一键扫描，选择规则组进行扫描。
    - feat（云账号）：优化云账号校验，输入空格自动格式化。
    - feat（云规则）：优化内置规则的默认描述。

!!! success "🐛 Bug修复 Bug Fixes"
    - fix（规则）：解决创建规则时，选择规则组进行过滤的问题。
    - fix（代理）：解决代理列表按proxyIp模糊查询的问题。
    - fix（统计分析）：解决云账号-统计分析-资源扫描，不合规资源数量查询重复的问题。
    - fix（统计分析）：解决云账号-统计分析-区域扫描查询结果不正确的问题。
    - fix（通知）：解决消息通知认证加密解密的问题。

v1.0.1
------------------------
2021年04月8日

!!! info "🌱 新功能 Features"
    - feat（系统设置）: 系统参数设置支持邮件设置，包含SMTP主机、端口、账户、密码配置。
    - feat（系统设置）: 系统设置支持消息通知，安全合规规则扫描资源通知，包含事件类型、接收人、邮件模板等配置。

!!! summary "🚀 性能优化 Optimization"
    - refactor（搜索）: 优化搜索，解决区分大小写与模糊查询的问题。
    - refactor（扫描规则）: 优化部分扫描规则的规则描述，解决描述不完整问题。
    - refactor（扫描结果）: 优化扫描结果列表，解决因表格字段过长显示串行问题。

!!! success "🐛 Bug修复 Bug Fixes"
    - fix（云账号）: 解决状态为无效的云账号也允许扫描的问题。
    - fix（扫描结果）: 解决云账号安全评分刷新慢的问题。
    - fix（翻译）: 解决部分中英文翻译不完整的问题。
    - fix（会话）: 修复登录时间过长未操作导致系统推出的问题。
    - fix（邮件）: 修复邮件模板显示格式不正确的问题。
