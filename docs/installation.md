# MongoDB部署指南

## ‌一、环境准备

### 一、更新系统

```bash
yum -y update  
yum -y upgrade
```

## ‌二、安装docker

参考：[安装Docker](https://support.huaweicloud.com/bestpractice-hce/hce_bp_0002.html)


## 三、拉取镜像和创建容器

### 1.拉取镜像
```bash
docker pull mongo:8.0.12
```

### 2.创建容器
```bash
docker run -d \
  --name mongodb \
  -p 27017:27017 \
  -e MONGO_INITDB_ROOT_USERNAME=admin \
  -e MONGO_INITDB_ROOT_PASSWORD=admin \
  mongo:8.0.12
```


