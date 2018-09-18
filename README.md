dev docker env
## 使用
前提

自行安装最新版本docker
====

## 目录结构
    .
    ├── README.md
    ├── docker-compose.yml	
    ├── logs							日志目录
    ├── nginx_default
    │   ├── Dockerfile				nginx build
    │   └── nginx.conf
    ├── php_fpm_72
    │   ├── Dockerfile				php7.2 build
    │   └── php.ini
    └── code                        存放代码的目录
        ├── conf					nginx各项目配置
        ├── other_project			非php代码目录，例如，golang | python
        └── php_project				php git代码目录


## 注意事项

windows 右下角 docker logo 右击弹框
Switch to Linux containers
Settings -> Shared Drives  在哪盘拉的代码哪个盘就要共享
#Settings -> Daemon -> Insecure registries 加上 192.168.1.156

手动拉git代码到web/src下
    git clone git@gitlab.xxx.xxx:ops/test_docker.git
    cd test_docker
    docker-compose up
    #docker-compose build || docker-compose up --build #修改容器镜像或增改配置 
