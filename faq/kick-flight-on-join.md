---
description: 玩家在下载资源包时被踢
---

# 🥾 加入服务器时被踢出提示飞行

## 问题描述

某些服务器可能会在资源包安装期间认为你正在飞行，这取决于你的出生点位置。

你可能会收到如下错误：<mark style="color:red;">"Flying is not enabled on this server"</mark>，或者被 **反作弊** 系统踢下线。

## 如何修复？

在 **ItemsAdder** 的 `config.yml` 文件中禁用 `hide-hud` 功能。

```yaml
  protect-player:
    black-screen: true
    hide-hud: false
```

## 仍然有问题

在 `server.properties` 文件中启用以下选项：

{% code title="server.properties" %}
```
allow-flight=true
```
{% endcode %}

此设置不会使玩家能够飞行，只是 Minecraft 服务器不会在没有权限的情况下踢出飞行的玩家。\
为了防止由于此设置而导致的作弊，建议使用 **AntiCheat** 插件。
