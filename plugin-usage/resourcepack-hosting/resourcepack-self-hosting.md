# 📥 自托管

## 视频教程

{% embed url="https://www.youtube.com/watch?v=XoTwF4_HztU" %}

## 关于自托管的信息

使用 ItemsAdder，您可以直接在您的服务器上托管资源包！\
不需要支付网站托管费用，并且 **每次更改时无需重新上传包！**

{% hint style="warning" %}
**您的托管服务必须允许您获取额外的端口。**\
如果您的托管服务不提供额外端口，您需要使用 [其他托管方法](./)。
{% endhint %}

### 自托管与其他方法的区别是什么？

区别在于，使用自托管时，您可以直接从您的服务器下载包，而不必在每次进行小改动时都上传到网站。

{% hint style="info" %}
`self-host` 在您在 PC 上的测试服务器上配置资源包时非常有用。因为您只需要使用命令 `/iazip`，就可以几乎立即在游戏中看到更改。
{% endhint %}

{% content-ref url="tips-for-fastest-usage.md" %}
[tips-for-fastest-usage.md](tips-for-fastest-usage.md)
{% endcontent-ref %}

## 如何配置自托管？

* 在您的 **托管服务面板** 中检查是否可以获取额外的端口，如果不能，请联系托管服务支持提供一个。

例如，在 **Pterodactyl** 上：

![](../../.gitbook/assets/image\_\(104\).png)

![](../../.gitbook/assets/image\_\(101\).png)

* 获得 **新端口** 后，您可以打开 `config.yml` 并按如下方式设置：

```yaml
  self-host:
    enabled: true
    server-ip: '127.0.0.1'
    pack-port: 8163
```

* 您需要将 `127.0.0.1` 替换为 **您的服务器 IP**
* 并将 `8163` 替换为您获得的新端口。

例如，如果我的 IP 是 `123.456.789.0` 且我的额外端口是 `8163`，我将设置如下：

```yaml
  self-host:
    enabled: true
    server-ip: '123.456.789.0'
    pack-port: 8163
```

{% hint style="warning" %}
**pack-port** 与您的服务器端口（用户用于连接的端口）不同。
{% endhint %}

{% hint style="info" %}
`127.0.0.1` 意味着 "**这台电脑**"。\
**所以如果您在您的 PC 上测试插件**，您可以 **保留默认配置**，这样插件将直接在您的 PC 上查找资源包 zip 文件。
{% endhint %}

{% hint style="danger" %}
不要忘记在每次编辑 **纹理**、**3D 模型**、**声音** 等后使用 `/iazip`，否则您将无法看到任何更改。
{% endhint %}

### 最后一步

在配置好 `config.yml` 文件后，您只需运行 `/iazip` 命令来刷新 zip 文件并启动托管。

## 如果需要继续安装

{% content-ref url="../../first-install.md" %}
[first-install.md](../../first-install.md)
{% endcontent-ref %}

## Cloudflare 付费计划

如果您使用 `Cloudflare` 来保护您的 IP + 端口（付费计划），并且您有一个特殊规则来将资源包请求从子域名重定向到资源包端口，请阅读以下部分。

例如：

* 服务器托管在 `mc.example.com`
* 资源包在端口 `8163`
* 您设置了 **Cloudflare** 规则，将所有流量从 `pack.example.com` 重定向到 `mc.example.com:8163`

为了使其正常工作，您需要将配置设置如下：

```yml
    self-host:
      enabled: true
      server-ip: 'https://pack.example.com' # <-- 别忘了 https
      pack-port: 8163
      append-port: false # <-- 重要
```

这将阻止 ItemsAdder 在您的 URL 前面添加 http，并阻止在 URL 末尾添加端口。
