# 升级文档

!!! warning "更新前请一定要做好备份工作"

### 升级步骤
=== "一键升级"
    !!! tip ""
        ```sh
        # 如果已经部署旧版本，可通过如下命令一键升级至最新版本:
        cd /opt/riskscanner-installer-v1.4.1  # v1.4.1 是版本号, 你的环境可能是其他的版本, 修改成对应的即可
        # 如果使用离线版本: cd /opt/riskscanner-offline-installer-v1.4.1

        ./rsctl.sh check_update
        ```

=== "在线升级"
    !!! tip ""
        ```sh
        cd /opt
        wget https://github.com/riskscanner/riskscanner-installer/releases/download/{{ riskscanner.version }}/riskscanner-installer-{{ riskscanner.version }}.tar.gz
        tar -xf riskscanner-installer-{{ riskscanner.version }}.tar.gz
        cd riskscanner-installer-{{ riskscanner.version }}
        ```
        ```sh
        ./rsctl.sh upgrade
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

        3. 清理镜像
        是否需要清理旧版本镜像文件? (y/n)  (默认为 n): y
        Untagged: x-lab/riskscanner:v1.3.0

        4. 升级成功, 可以重启程序了
        cd /opt/riskscanner-installer-{{ riskscanner.version }}
        ./rsctl.sh restart
        ```
        ```sh
        ./rsctl.sh down
        ./rsctl.sh start
        ```

=== "离线升级"
    !!! tip ""
        从飞致云社区 [下载最新的离线包](https://community.fit2cloud.com/#/products/riskscanner/downloads){:target="_blank"}, 并上传到部署服务器的 /opt 目录

    !!! tip ""
        ```sh
        cd /opt
        unzip riskscanner-offline-installer-{{ riskscanner.version }}.zip
        cd riskscanner-offline-installer-{{ riskscanner.version }}
        ```
        ```sh
        ./rsctl.sh upgrade
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

        3. 清理镜像
        是否需要清理旧版本镜像文件? (y/n)  (默认为 n): y
        Untagged: x-lab/riskscanner:v1.3.0

        4. 升级成功, 可以重启程序了
        cd /opt/riskscanner-offline-installer-{{ riskscanner.version }}
        ./rsctl.sh restart
        ```
        ```sh
        ./rsctl.sh down
        ./rsctl.sh start
        ```
