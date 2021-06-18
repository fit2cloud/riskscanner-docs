# 升级文档

!!! warning "更新前请一定要做好备份工作"

### 升级步骤

!!! tip "操作步骤"
    ```sh
    cd /opt
    yum -y install wget
    wget https://github.com/riskscanner/riskscanner-installer/releases/download/{{ riskscanner.version }}/riskscanner-installer-{{ riskscanner.version }}.tar.gz
    tar -xf riskscanner-installer-{{ riskscanner.version }}.tar.gz
    cd riskscanner-installer-{{ riskscanner.version }}
    ```
    ```sh
    ./jmsctl.sh upgrade
    ```
    ```nginx hl_lines="1 35"
    是否将版本更新至 {{ riskscanner.version }} ? (y/n)  (默认为 n): y

    1. 升级镜像文件
    Docker: Pulling from x-lab/mysql:5.7.31 	        [ OK ]
    Docker: Pulling from x-lab/riskscanner:{{ riskscanner.version }} 	    [ OK ]
    完成

    2. 备份数据库
    正在备份...
    mysqldump: [Warning] Using a password on the command line interface can be insecure.
    [SUCCESS] 备份成功! 备份文件已存放至: /opt/riskscanner/db_backup/riskscanner-2021-03-19_08:32:39.sql

    3. 升级成功, 可以重启程序了
    ./jmsctl.sh restart
    ```
    ```sh
    ./jmsctl.sh restart
    ```
