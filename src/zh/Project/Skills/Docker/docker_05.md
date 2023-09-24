---
title: Docker 删除所有悬虚镜像
order: 5
category:
  - Project
  - Skills
  - Docker
  - MD
---

## 1.1 什么是 悬虚镜像

悬虚镜像就是镜像没有仓库名或没有标签查询显示虚悬镜像，在列表中展示为 `<none>:<none>`
## 1.2 悬虚镜像 怎么来的

有时候在构建新镜像的时候，为这个镜像打了一个已经存在的tag，此时 Docker 会移除旧镜像上的 tag,将这个 tag 用在新的镜像上，此时旧镜像就变成了悬虚镜像, 或者构建新镜像报错时，也会生成一个悬虚镜像。
## 1.3 删除悬虚镜像

```docker
docker image prune
```

::: warning
此处因为我刚清理过 so ~
:::

![](https://yong-gan-niu-niu-1311841992.cos.ap-beijing.myqcloud.com/images/20230923225139.png) 



