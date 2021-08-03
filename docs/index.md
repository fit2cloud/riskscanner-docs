# 总体介绍

!!! tip ""
    RiskScanner `/ˈrɪskˌskænə(r)/` 是开源的多云安全合规扫描平台，使用 GPL v2 开源协议。

    RiskScanner 使用 SpringBoot/Vue 进行开发，界面美观、用户体验好。

    RiskScanner 是开源的多云安全合规扫描平台，基于 Cloud Custodian 和 Nuclei 引擎，实现对主流公(私)有云资源的安全合规扫描和漏洞扫描。

    RiskScanner 支持的公有云包括阿里云、腾讯云、华为云、Amazon Web Services、Microsoft Azure、Google Cloud，支持的私有云包括 OpenStack、VMware vSphere 等， 并且支持漏洞扫描。

## 架构图

![RiskScanner功能架构图](img/intro/functional-architecture.png)

## 功能优势

!!! tip ""
    - 等保 2.0 预检：符合等保 2.0 规范，覆盖安全审计、访问控制、入侵防范、网络架构和管理中心等各项检查；
    - CIS 合规检查：符合 CIS 规范，检查和实时监控在云上的资源是否符合 CIS 要求；
    - 漏洞扫描：通过对网络的扫描，发现可利用漏洞的安全检测（渗透攻击）；
    - 最佳实践建议：制定合规管控基线，为企业级用户提供最佳实践建议，持续提升合规水平；

## 技术优势

!!! tip ""
    - 规则简单灵活：扫描规则采用简单的 YAML 格式，简单易懂、并允许用户自定义规则；
    - 支持多公/私有云：支持的公有云包括阿里云、腾讯云、华为云、Amazon Web Services、Microsoft Azure、Google Cloud，支持的私有云包括 OpenStack、VMware vSphere 等；
    - 支持多资源：支持的资源类型包括云服务器、云磁盘、云数据库、负载均衡、对象存储、专有网络、安全组等；
    - 漏洞扫描：可配置攻击目标，零误报，包含了爬虫、通用漏洞检测（如 SQL 注入、XSS 检测）、指纹信息收集（如 Web 服务、语言框架等）、专用漏洞检测等；

## 页面展示

![UI 界面展示](./img/intro/dashboard.png)
