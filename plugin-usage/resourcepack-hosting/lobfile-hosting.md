# 📤 用LobFile托管

{% hint style="warning" %}
此功能需要 **ItemsAdder 3.6.3** 或更高版本。
{% endhint %}

（翻译者：我**强烈不建议**使用该方法作为第三方托管，因为国内可能会出现墙或是下载过慢，建议使用**自托管**或是寻找其他稳定的文件托管平台，我用过Github和Gitee）

## 什么是 LobFile？

**ItemsAdder** 允许您将资源包自动上传到一个 **免费的在线服务**，该服务在全球范围内提供服务器。

非常感谢 **LobFile** [这里](https://ploudos.com/it/)，他们为我们提供了免费托管文件的平台！

{% embed url="https://lobfile.com/" %}

{% hint style="warning" %}
### 警告

此托管方法的文件大小限制为 100MB。
{% endhint %}

## 有什么优势？

* 下载速度
* 可用性
* 安全性：您的服务器 IP 地址不会被公开
* 不会消耗大量带宽

## 我已经在使用 `self-host`，这个更好吗？

要看情况。

如果您正在开发资源包，并且需要不断运行 `/iazip`，以避免浪费时间（详细信息见 [这里](tips-for-fastest-usage.md)），那么使用 [self-host](resourcepack-self-hosting.md) 会更好。

当您完成资源包的工作后，您可以安全地开始使用其他托管功能而不是 `self-host`，在这种情况下就是 **LobFile**。\
这样可以减少服务器的流量，因为资源包将不再托管在您的服务器上。\
不过，如果您的玩家群体都来自同一国家，您可以继续使用 `self-host`。

## 设置

#### 第一步

在 [LobFile 这里](https://lobfile.com/create-account) 创建一个账户。

#### 第二步

打开您的 [账户设置](https://lobfile.com/my-account) 并勾选 _**"Continuous uploading"**_

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

#### 第三步

悬停在 `API Key` 文本上并复制您的密钥。

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

#### 第四步

在 `config.yml` 中启用 `lobfile` 并禁用所有其他托管方法。

{% code title="ItemsAdder/config.yml" %}
```yaml
lobfile:
  enabled: true
```
{% endcode %}

打开 `secret.yml` 并粘贴您的 `API Key`。

{% code title="ItemsAdder/secret.yml" %}
```yaml
lobfile:
  api_key: xxxxxxxxxx
```
{% endcode %}

#### 第五步

运行 `/iazip.`

等待隐私政策消息出现。\
运行 `/acceptprivacy` 接受政策（只会在第一次时要求）。

### 完成

**插件** 将 **自动上传** 资源包到网上。\
无需其他操作，享受您的 **免费自动化资源包托管**。

## 我的资源包会对随机用户开放吗？

2023-12-21：\
您的资源包不会被 Google 索引，也不会被发布在资源包列表中。\
只有知道链接的人才能下载该包。
