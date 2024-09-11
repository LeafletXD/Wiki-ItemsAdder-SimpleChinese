---
description: 在 Bungeecord 网络中使用单一资源包，并为每个服务器禁用单独的功能
---

# 全局资源包，但不同的功能（Bungeecord）

教程作者 [@itsmemac](https://github.com/LoneDev6/Wiki-ItemsAdder/pull/35)

{% hint style="info" %}
在按照本指南操作之前，请确保已完成 [**首次安装**](https://itemsadder.devs.beer/first-install) 并拥有一个正常运行的 IA 安装。
{% endhint %}

**步骤 1**

在本地创建包含整个网络中所需内容的最终资源包（包括每个物品、GUI、怪物、表情符号等）。  
为此，你需要在电脑上创建一个本地 Spigot 服务器，并配置所需的一切。

**步骤 2**

打开每个 Spigot 服务器，在 ItemsAdder 配置中将托管方法设置为 `no-host`，并将提取物品功能禁用（设为 false）。

{% code title="config.yml" %}
```yaml
  hosting:
    no-host:
      enabled: true
  extract-default-items: false
  extract-default-resources: false
```
{% endcode %}

**步骤 3**

运行 `/iazip` 并将生成的资源包上传到一个提供直接下载链接的文件托管服务。  
例如 [**MCPACKS**](https://mc-packs.net/)、[**DropBox**](../../plugin-usage/resourcepack-hosting/resourcepack-on-dropbox.md)、[**GoogleDrive**](../../plugin-usage/resourcepack-hosting/google-drive-1.17.1+.md) 等。

**步骤 4**

使用 [**Force resourcepack**](https://www.spigotmc.org/resources/force-resourcepacks.10499/) 或类似插件，在玩家进入网络时加载资源包。

**步骤 5**

将 `ItemsAdder.jar` 和整个 `ItemsAdder` 插件文件夹从本地 Spigot 服务器复制到网络中的第一个服务器（例如 `lobby`），放入其 `/plugins` 文件夹中。

**步骤 6**

打开 ItemsAdder 的 `config.yml`，禁用你不需要的功能。  
同时，从 `plugins/ItemsAdder/contents/` 文件夹中删除不需要的文件。

{% hint style="danger" %}
不要删除 `dictionaries`、`mcemojis`、`mcguis`、`mcicons`、`realcraft`、`various_configs` 文件夹。  
阅读更多：[删除ItemsAdder的默认物品](../removing-default-stuff/)
{% endhint %}

基本上，你需要保留你想在该特定服务器（例如 `lobby`）中保留的功能文件夹。

**步骤 7**

重启服务器并加入，服务器会要求你下载资源包。  
你将只能看到 `contents` 文件夹中保留的物品。

**步骤 8**

为网络中的每个服务器重复步骤 5、6、7。

{% hint style="info" %}
本教程不需要使用 **BungeePackFix** 插件。
{% endhint %}
