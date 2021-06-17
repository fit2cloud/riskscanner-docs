# 更新日志

## 版本说明
Riskscanner 版本号命名规则为：v大版本.功能版本.Bug修复版本

"例如"

    v1.0.1 是 v1.0.0 之后的Bug修复版本

    v1.1.0 是 v1.0.0 之后的功能版本
------------------------------------------------------------------------


## v1.0.0
# 快速开始
仅需两步快速安装 RiskScanner：
1.  准备一台不小于 4 G内存的 64位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。
```sh
  curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```
# 产品文档
点击 [完整文档](https://docs.riskscanner.io/) 查看完整的安装和使用文档
# 离线安装包
百度网盘下载链接: https://pan.baidu.com/s/10AKnB4a1dVLIlObP4inBhg  密码: 4rwe

------------------------------------------------------------------------

## v1.0.1
# 快速开始
仅需两步快速安装 RiskScanner：
1.  准备一台不小于 4 G内存的 64位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。
```sh
  curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```
# 产品文档
点击 [完整文档](https://docs.riskscanner.io/) 查看完整的安装和使用文档
# 离线安装包
百度网盘下载链接: https://pan.baidu.com/s/1lfVSb2ZtO59lwY3irL82aQ  密码: 4gs4

## 新增功能

- feat（系统设置）： 系统参数设置支持邮件设置，包含SMTP主机、端口、账户、密码配置。
- feat（系统设置）： 系统设置支持消息通知，安全合规规则扫描资源通知，包含事件类型、接收人、邮件模板等配置。

## 功能优化

- refactor（搜索）：优化搜索，解决区分大小写与模糊查询的问题。
- refactor（扫描规则）：优化部分扫描规则的规则描述，解决描述不完整问题。
- refactor（扫描结果）：优化扫描结果列表，解决因表格字段过长显示串行问题。

## Bug 修复

- fix（云账号）：解决状态为无效的云账号也允许扫描的问题。
- fix（扫描结果）：解决云账号安全评分刷新慢的问题。
- fix（翻译）：解决部分中英文翻译不完整的问题。
- fix（会话）：修复登录时间过长未操作导致系统推出的问题。
- fix（邮件）：修复邮件模板显示格式不正确的问题。

------------------------------------------------------------------------

## v1.1.0
# 快速开始
仅需两步快速安装 RiskScanner：
1.  准备一台不小于 4 G内存的 64位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。
```sh
  curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```
# 产品文档
点击 [完整文档](https://docs.riskscanner.io/) 查看完整的安装和使用文档
# 离线安装包
百度网盘下载链接: https://pan.baidu.com/s/1pyvxDmFa3fl87Jjl0UgFXA  密码: wtfk

## 新增功能
- feat（云账号）：新增 Amazon Web Services 云平台，内置扫描规则、规则组，支持 AWS 国际区、中国区平台资源的扫描。
- feat（云账号）：新增 Microsoft Azure 云平台，内置扫描规则、规则组，支持 Azure 中国区、国际区、美国区、德国区平台资源的扫描。
- feat（代理）：新增 http/https 代理配置，云账号绑定并启用代理。
- feat（通知）：新增消息通知类型，钉钉通知。
- feat（通知）：新增消息通知类型，企业微信通知。

## 功能优化
- feat（云账号）：优化添加云账号，可批量添加云账号。
- feat（云账号）：优化一键扫描，选择规则组进行扫描。
- feat（云账号）：优化云账号校验，输入空格自动格式化。
- feat（云规则）：优化内置规则的默认描述。

## Bug 修复
- fix（规则）：解决创建规则时，选择规则组进行过滤的问题。
- fix（代理）：解决代理列表按proxyIp模糊查询的问题。
- fix（统计分析）：解决云账号-统计分析-资源扫描，不合规资源数量查询重复的问题。
- fix（统计分析）：解决云账号-统计分析-区域扫描查询结果不正确的问题。
- fix（通知）：解决消息通知认证加密解密的问题。

------------------------------------------------------------------------

## v1.1.1
# 快速开始
仅需两步快速安装 RiskScanner：
1.  准备一台不小于 4 G内存的 64位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。
```sh
  curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```
# 产品文档
点击 [完整文档](https://docs.riskscanner.io/) 查看完整的安装和使用文档
# 离线安装包
百度网盘下载链接: https://pan.baidu.com/s/1KLB2oXUmpoy-Z4UOnxTMfw  密码: fl2d

## BUG 修复
- 解决登录页面报错，弹框认证信息已过期的问题。

------------------------------------------------------------------------

## v1.2.0
# 快速开始
仅需两步快速安装 RiskScanner：
1.  准备一台不小于 4 G内存的 64位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。
```sh
  curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```
# 产品文档
点击 [完整文档](https://docs.riskscanner.io/) 查看完整的安装和使用文档
# 离线安装包
百度网盘下载链接: https://pan.baidu.com/s/1DhIybJGOXcggUvQ7cscwMQ  密码: to96

## 新增功能
- feat（云账号）：新增 OpenStack 私有云平台，内置扫描规则、规则组，支持平台资源的扫描。
- feat（云账号）：新增 VMware vSphere 私有云平台，内置扫描规则、规则组，支持平台资源的扫描。
- feat（扫描结果）：新增安全合规报告下载功能。

## 功能优化
- feat（云账号）：优化 aws、azure、aliyun、huawei、tencent 等平台 IAM 策略信息。
- feat（扫描规则）：优化规则组与规则的显示，点击规则组显示对应的规则列表。
- feat（云账号）：新增 VMware vSphere 私有云平台，内置扫描规则、规则组，支持平台资源的扫描。

## Bug 修复
- fix（扫描结果）：解决优化改进建议不正确的问题。
- fix（扫描结果）：解决扫描结果按规则组维度显示的问题。
- fix（云账号）：解决 IAM 策略信息的导入云平台报错问题。
- fix（云账号）：解决一键扫描未扫描已保存的参数的问题。

------------------------------------------------------------------------

## v1.2.1
# 快速开始
仅需两步快速安装 RiskScanner：
1.  准备一台不小于 4 G内存的 64位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。
```sh
  curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```
# 产品文档
点击 [完整文档](https://docs.riskscanner.io/) 查看完整的安装和使用文档
# 离线安装包
百度网盘下载链接: https://pan.baidu.com/s/16ASYulpHXW5HpAvyJgwv5Q  密码: m5am

## 新增功能
- feat（云账号）：新增定时任务功能（定时扫描某些云账号或某些规则）。
- feat（API）：新增 RiskScanner Restful APIs 测试用例。

## 功能优化
- feat（扫描规则）：优化各个云平台安全组的规则，比如规则似乎是将条件解释为OR而不是AND。优化VMware vSphere VM/ResourcePool 扫描规则。
- feat（扫描结果）：优化后端性能，提升扫描速度，降低扫描时间。
- feat（云账号）：优化云账号校验，无效状态校验提示失败。

## Bug 修复
- fix（云账号）：解决 Azure 国际区账户验证失败的问题。
- fix（扫描结果）：解决扫描结果按规则组维度显示的问题。
- fix（云账号）：解决 IAM 策略信息的导入云平台报错问题。
- fix（云账号）：解决 Azure 国际区账户验证失败的问题。

------------------------------------------------------------------------
