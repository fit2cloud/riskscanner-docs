# 安装文档

!!! info "说明"
    全新安装的 Linux(x64)  
    需要连接 互联网  
    使用 root 用户执行

## 安装方式

!!! info "外置环境要求"
    - 推荐使用外置 数据库, 方便日后扩展升级

| DB      | Version |
| :------ | :------ |
| MySQL   | >= 5.7  |
| MariaDB | >= 10.2 |


=== "自动部署"
    !!! tip ""
        ```sh
        curl -sSL https://github.com/riskscanner/riskscanner/releases/download/{{ riskscanner.version }}/quick_start.sh | bash
        ```

=== "手动部署"
    !!! tip ""
        ```sh
        cd /opt
        wget https://github.com/riskscanner/riskscanner-installer/releases/download/{{ riskscanner.version }}/riskscanner-installer-{{ riskscanner.version }}.tar.gz
        tar -xf riskscanner-installer-{{ riskscanner.version }}.tar.gz
        cd riskscanner-installer-{{ riskscanner.version }}
        cat config-example.txt
        ```

    ???+ info "配置文件说明"
        ```vim
        # 以下设置如果为空系统会自动生成随机字符串填入

        ## 安装配置
        DOCKER_IMAGE_PREFIX=registry.cn-qingdao.aliyuncs.com
        VOLUME_DIR=/opt/riskscanner
        DOCKER_DIR=/var/lib/docker

        ## Compose 项目设置
        COMPOSE_PROJECT_NAME=rs
        COMPOSE_HTTP_TIMEOUT=3600
        DOCKER_CLIENT_TIMEOUT=3600

        ##  MySQL 配置, USE_EXTERNAL_MYSQL=1 表示使用外置数据库, 请输入正确的 MySQL 信息
        USE_EXTERNAL_MYSQL=0
        DB_HOST=mysql
        DB_PORT=3306
        DB_USER=root
        DB_PASSWORD=
        DB_NAME=riskscanner

        ## Service 端口
        HTTP_PORT=80

        # 额外的配置
        CURRENT_VERSION=
        ```

=== "离线部署"

    | 下载地址                                                                                                                                                | 密码 |
    | :----------------------------------------------------------------------------------------------------------------------------------------------------- | :--- |
    | [百度网盘](https://pan.baidu.com/s/1TqYggL7AWiUrIV-fOtfwNA 密码: jd90)                                                                                             | jd90 |
    下载完成后，上传到 linux 服务器 /opt 目录进行解压

    !!! tip ""
        ```bash
        unzip riskscanner-release-{{ riskscanner.version }}-offline.zip
        cd riskscanner-release-{{ riskscanner.version }}-offline
        ./rsctl.sh install
        ```

## 使用方式

- 安装目录 /opt/riskscanner-installer-{{ riskscanner.version }}
- 配置文件 /opt/riskscanner/config/config.txt

!!! tip "安装"
    ```sh
    ./rsctl.sh install
    ```

!!! tip "启动"
    ```sh
    ./rsctl.sh start
    ```

!!! tip "关闭"
    ```sh
    ./rsctl.sh down
    ```

!!! tip "帮助"
    ```sh
    ./rsctl.sh -h
    ```

!!! tip "默认登录密码："
    ```sh
    admin/riskscanner
    ```
