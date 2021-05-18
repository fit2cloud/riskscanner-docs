# 快速开始

## 准备工作

仅需两步快速安装 RiskScanner：

1.  准备一台不小于 4 G 内存的 64 位 Linux 主机；
2.  以 root 用户执行如下命令一键安装 RiskScanner。

#### 一、快速安装

```sh
curl -sSL https://github.com/riskscanner/riskscanner/releases/latest/download/quick_start.sh | sh
```

#### 二、离线安装

```sh
# 以下方式任选一种即可：
# 1、获取百度网盘离线安装包，百度网盘下载链接: https://pan.baidu.com/s/1KLB2oXUmpoy-Z4UOnxTMfw 密码: fl2d
# 2、获取 OSS 离线安装包，wget https://fit2cloud2-offline-installer.oss-cn-beijing.aliyuncs.com/riskscanner/riskscanner-release-1.1.1-offline.tar.gz
# 解压安装包
tar zxvf riskscanner-release-1.1.1.tar.gz
# 进入解压包
cd riskscanner-release-1.1.1
# 执行脚本
./install.sh
# 查看运行状态
rsctl status
```

#### 三、在线安装

```sh
# 以下方式任选一种即可：
# 1、在 https://github.com/riskscanner/riskscanner/releases/tag/v1.1.1 页面下载 github release 最新在线安装包
# 2、获取 OSS 在线安装包，wget https://fit2cloud2-offline-installer.oss-cn-beijing.aliyuncs.com/riskscanner/riskscanner-release-1.1.1.tar.gz
# 解压安装包
tar zxvf riskscanner-release-1.1.1.tar.gz
# 进入解压包
cd riskscanner-release-1.1.1
# 执行脚本
./install.sh
# 查看运行状态
rsctl status
```

!!! info "安装完成之后 RiskScanner 会以名字为 `RiskScanner` 服务的形式存在会有如下命令"
    - rsctl  status    查看 RiskScanner 服务运行状态
    - rsctl  start     启动 RiskScanner 服务
    - rsctl  stop      停止 RiskScanner 服务
    - rsctl  restart   重启 RiskScanner 服务
    - rsctl  reload    重新加载 RiskScanner 服务
    - rsctl  uninstall 卸载 RiskScanner 服务
    - rsctl  version   查看 RiskScanner 版本信息
    
## 登录并使用

### 登录

#### Login 界面

![Login 界面说明](./img/quickstart/login.png)

安装成功后，通过浏览器访问如下页面登录 RiskScanner

```
地址: http://目标服务器IP地址:8080
用户名: admin
密码: riskscanner
```

### 界面说明

RiskScanner 公有云安全合规平台 UI 及交互遵循 Material Design 及 UI 规范，基于统一规范进行开发，提供一致的操作体验。

#### UI 主界面

![UI 主界面说明](./img/quickstart/use.png)



