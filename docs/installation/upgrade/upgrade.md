# 升级文档

!!! warning "更新前请一定要做好备份工作"

### 升级步骤
=== "快速在线升级"
    ```sh
    #如果您已经部署旧版本，可通过如下命令一键升级至最新版本:
    cd /opt/riskscanner
    # 直接升级并且自动重启，无需其他操作
    ./rsctl.sh check_update
    ```

=== "在线升级"
    ```sh
    cd /opt
    wget https://github.com/riskscanner/riskscanner-installer/releases/download/{{ riskscanner.version }}/riskscanner-installer-{{ riskscanner.version }}.tar.gz
    tar -xf riskscanner-installer-{{ riskscanner.version }}.tar.gz
    cd riskscanner-installer-{{ riskscanner.version }}
    ```

=== "离线升级"

    | 下载地址                                                                                                                                                | 密码 |
    | :----------------------------------------------------------------------------------------------------------------------------------------------------- | :--- |
    | [百度网盘](https://pan.baidu.com/s/1TqYggL7AWiUrIV-fOtfwNA 密码: jd90)                                                                                             | jd90 |
    ```bash
    # 下载到 /opt 目录
    cd /opt
    unzip riskscanner-release-{{ riskscanner.version }}-offline.zip
    cd riskscanner-release-{{ riskscanner.version }}-offline
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
./rsctl.sh restart
```
```sh
./rsctl.sh down
./rsctl.sh start
```
