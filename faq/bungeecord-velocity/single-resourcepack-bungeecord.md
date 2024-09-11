---
描述: 使用全局资源包，避免玩家在每次加入服务器时重新下载资源包
---

# 全局资源包（Bungeecord）

## 全局资源包

你想在网络中的多个 Spigot 服务器上安装 ItemsAdder 吗？  
你想避免玩家每次切换服务器时都下载资源包吗？  
请按照这个简单的教程操作。

## 设置方法

例如，你可以有 3 个服务器：`lobby`、`survival`、`creative`。

### 第一步

在这 3 个服务器上安装 ItemsAdder。

{% hint style="warning" %}
<mark style="color:red;">**这非常重要！**</mark>

每次进行修改时，请确保**同步所有** 3 个服务器的 `plugins/ItemsAdder/` **配置文件夹**，它们必须相同，只有 `config.yml` 的托管部分可以不同。

这是此任务的关键步骤，否则将无法正常工作。
{% endhint %}

### 第二步

决定一个主服务器，例如 `lobby`。  
打开 `lobby` 服务器中 ItemsAdder 的 `config.yml` 文件，并设置托管部分。

{% content-ref url="../../plugin-usage/resourcepack-hosting/" %}
[resourcepack-hosting](../../plugin-usage/resourcepack-hosting/)
{% endcontent-ref %}

{% hint style="info" %}
建议使用 `self-host`，这是最好的方法。
{% endhint %}

在完成托管配置后（仔细按照链接的教程操作），使用 `/iainfo` 命令，在控制台获取 URL，并复制它。

例如：

![](<../../.gitbook/assets/image (60) (1).png>)

{% hint style="warning" %}
必须删除 `#` 之后的 URL 部分，它并不是必需的。  
复制时请忽略 `#` 后的部分。
{% endhint %}

#### 例如使用 `self-host`：

<details>

<summary>自托管示例</summary>

{% code title="config.yml" %}
```yaml
resource-pack:
  hosting:
    no-host:
      enabled: false
    auto-external-host:
      enabled: false
    self-host:
      enabled: true
      server-ip: YOUR_SERVER_IP_HERE
      pack-port: 8163
    external-host:
      enabled: false
      url: ''
```
{% endcode %}

运行 `/iazip` 以生成资源包。

</details>

### 第三步

打开其他服务器（survival、creative）的 ItemsAdder `config.yml` 文件，并编辑托管部分。  
将 `/iainfo` 命令获得的 **URL** 填入 `YOUR_PACK_COMPLETE_URL` 的位置。

{% code title="config.yml" %}
```yaml
resource-pack:
  hosting:
    no-host:
      enabled: false
    auto-external-host:
      enabled: false
    self-host:
      enabled: false
      server-ip: 127.0.0.1
      pack-port: 8163
    external-host:
      enabled: true
      url: 'YOUR_PACK_COMPLETE_URL'
```
{% endcode %}

### 第四步（仅限 Bungeecord）

安装 Bungeecord 插件，以使加载速度更快！

{% embed url="https://www.spigotmc.org/resources/96794" %}

{% hint style="danger" %}
<mark style="color:red;">**不要在**</mark> <mark style="color:red;">**Spigot**</mark> <mark style="color:red;">**服务器上安装**</mark> <mark style="color:red;">**BungeePackFix**</mark>！

这是一个 **Bungeecord** 插件！请安装在 **Bungeecord** 上！
{% endhint %}
