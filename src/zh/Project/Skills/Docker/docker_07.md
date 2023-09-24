---
title: WebStorm + Docker 快速部署 Nginx 项目
order: 7
category:
  - Project
  - Skills
  - Docker
  - MD
---

## 一、 WebStorm 中 Docker 的配置

可参考 [IDEA + Docker 快速部署 Spring Boot 项目](./docker_06.md) 中的配置，过程基本相同。

## 二、快速部署 Nginx 项目

这部分 Dockerfile 的创建及启动脚本的配置基本类似我们讲解下流程即可：

Nginx 在配置过程中需要手动配置 `nginx.conf` 等信息

- [下载 Nginx 配置文件](https://yong-gan-niu-niu-1311841992.cos.ap-beijing.myqcloud.com/tools/conf.zip) 并存放与项目中

![image-20230924163455499](https://yong-gan-niu-niu-1311841992.cos.ap-beijing.myqcloud.com/images/image-20230924163455499.png)

- 配置 nginx 相关信息例如 port

![image-20230924163439688](https://yong-gan-niu-niu-1311841992.cos.ap-beijing.myqcloud.com/images/image-20230924163439688.png)

- Dockerfile 文件

```dockerfile
FROM nginx

# 映射 HTML
COPY ./src/.vuepress/dist ./usr/share/nginx/html
# Conf

COPY src/.vuepress/dist/conf/nginx.conf ./etc/nginx/conf.conf
COPY src/.vuepress/dist/conf/conf.d ./etc/nginx/conf.d

EXPOSE 80
```

## 三、验证

此处以 `vue-hope` 为基础模板进行操作 关于 `vue-hope` 此处可参照 [Vue-Hope 模板](../../HelloWorld/Vue-Hope) 中的内容 （帮你快速搭建一个 基于 Vue3 的 Blog）

TODO

