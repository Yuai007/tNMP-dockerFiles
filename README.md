# tNMP-dockerFiles

tNMP-dockerFiles for windows or linux.

## 简介

用docker容器服务的方式搭建tNMP环境。简单便捷迅速。composer已经默认使用阿里云镜像。

## 各组件版本:

* PHP:7.2
* MySql:5.7
* Nginx:1.12
* Redis:3.2

用到的PHP扩展

* redis 3.1.4
* swolle：4.5.0

## 使用:

### 1.安装 Docker，Docker-compose

- Docker，详见官方文档：https://docs.docker.com/engine/installation/linux/docker-ce/centos/
- docker-compose，文档：https://docs.docker.com/compose/install/

### 2.docker-compose 构建项目

进入 docker-compose.yml 所在目录：
执行命令：

```
docker-compose up
```
### 3. 使用 Composer

先获取docker容器列表

```
docker ps -a
```

再进入到php-fpm容器

```
docker exec -it files_php-fpm_1 bash
```

最后直接使用Composer命令

```
composer install
```

