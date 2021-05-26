## 环境要求

!!! info "部署服务器推荐"
    * 操作系统: CentOS 7.x
    * CPU/内存: 2核4G及以上
    * 磁盘空间: 100G

## 下载安装包

请自行下载 RiskScanner 最新版本的离线安装包，并复制到目标机器的 /tmp 目录下

## 解压安装包

以 root 用户 ssh 登录到目标机器, 并执行如下命令

```sh
cd /tmp
# 解压安装包
tar zxvf riskscanner-release-1.2.0-offline.tar.gz
```

## 修改安装配置

在安装包解压后的目录，编辑修改安装参数

```sh
cd riskscanner-release-1.2.0-offline
vim install.conf
```

其他参数可使用默认值


!!! info "安装配置文件说明, 如果无特殊需求可以不进行修改采用默认参数安装"
    ```vim
    # 基础配置
    ## 安装目录
    RS_BASE=/opt
    ## 镜像 prefix
    RS_PREFIX=registry.fit2cloud.com/riskscanner
    ## riskscanner tag
    RS_TAG=1.2.0
    ## Service 端口
    RS_PORT=8080
    
    # 数据库配置
    ## 是否使用外部数据库
    RS_EXTERNAL_MYSQL=false
    ## 数据库地址
    RS_MYSQL_HOST=mysql
    ## 数据库端口
    RS_MYSQL_PORT=3306
    ## RiskScanner 数据库库名
    RS_MYSQL_DB_RS=riskscanner
    ## 数据库用户名
    RS_MYSQL_USER=root
    ## 数据库密码
    RS_MYSQL_PASSWORD=Password123@mysql
    ```

!!! info "注意"
    如果使用外部数据库进行安装，推荐使用 MySQL 5.7 版本。同时 RiskScanner 对数据库部分配置项有要求，请参考下附的数据库配置，修改环境中的数据库配置文件

    ```
    [mysqld]
    datadir=/var/lib/mysql
    default-storage-engine=INNODB
    character_set_server=utf8
    lower_case_table_names=1
    table_open_cache=128
    max_connections=2000
    max_connect_errors=6000
    innodb_file_per_table=1
    innodb_buffer_pool_size=1G
    max_allowed_packet=64M
    transaction_isolation=READ-COMMITTED
    innodb_flush_method=O_DIRECT
    innodb_lock_wait_timeout=1800
    innodb_flush_log_at_trx_commit=0
    sync_binlog=0
    sql_mode=STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_AUTO_CREATE_USER,NO_ENGINE_SUBSTITUTION
    skip-name-resolve

    [mysql]
    default-character-set=utf8

    [mysql.server]
    default-character-set=utf8
    ```

    请参考文档中的建库语句创建 RiskScanner 使用的数据库，RiskScanner 服务启动时会自动在配置的库中创建所需的表结构及初始化数据。
    ```mysql
    CREATE DATABASE `riskscanner` /*!40100 DEFAULT CHARACTER SET utf8mb4 */;
    ```

安装脚本默认使用 /opt/riskscanner 目录作为安装目录，RiskScanner 的配置文件、数据及日志等均存放在该安装目录

## 执行安装脚本

```sh
# 进入安装包目录
cd riskscanner-release-1.2.0-offline
# 运行安装脚本
/bin/bash install.sh
# 等待安装脚本执行完成后，查看 RiskScanner 状态
rsctl status
```

安装成功后，通过浏览器访问如下页面登录 RiskScanner

```
地址: http://目标服务器IP地址:8080
用户名: admin
密码: riskscanner
```

