# 📤 用Google Drive托管 (1.17.1+)

## 如何使用 Google Drive

{% hint style="warning" %}
由于 Minecraft 的一个错误，此方法在 Minecraft 1.17 版本之前的一些 PC 上存在问题，更多信息请参见：[https://bugs.mojang.com/browse/MC-143768](https://bugs.mojang.com/browse/MC-143768)

此方法在 Minecraft 1.17.1 及更高版本中 100% 有效。
{% endhint %}

（翻译者：我**强烈不建议**使用该方法作为第三方托管，建议使用**自托管**或是寻找其他稳定的文件托管平台，我用过Github和Gitee）

### 第一步

右键点击您的资源包 zip 文件，然后点击“获取链接”

![](<../../.gitbook/assets/image\_(153) (1).png>)

### 第二步

重要：将权限设置为“任何拥有链接的人”

![](../../.gitbook/assets/image\_\(145\).png)

点击“复制链接”

![](../../.gitbook/assets/image\_\(149\).png)

### 第三步

访问以下网站：[http://a.devs.beer/gdrive-direct](http://a.devs.beer/gdrive-direct)

粘贴链接并点击“获取直接链接”

<img src="../../.gitbook/assets/image_(144).png" alt="" data-size="original">

### 第四步

该网站会自动将生成的链接添加到您的剪贴板中。

![](../../.gitbook/assets/image\_\(147\).png)

您现在可以将链接粘贴到 **ItemsAdder** 配置文件 `config.yml` 中，然后使用 `/iareload` 命令。

{% code title="config.yml" %}
```yaml
external-host:
  enabled: true
  url: 'http://drive.google.com/uc?export=view&id=10g3whim95Hab40KZNjUkwY9FUuqKMGh5'
```
{% endcode %}

### 完成！

您现在可以看到游戏已正确加载了资源包。

## 常见问题

### 在“Making Request... 100%”上等待时间过长

### ![](../../.gitbook/assets/image\_\(141\).png)

这是正常的。发生这种情况是因为 Google Drive 在授权下载资源包之前需要做一些处理。

这仅在玩家第一次下载资源包时发生，通常需要 5 到 10 秒钟。

### 资源包完全无法加载

由于 Minecraft 的一个错误，此方法在 Minecraft 1.17 版本之前的一些 PC 上存在问题，更多信息请参见：[https://bugs.mojang.com/browse/MC-143768](https://bugs.mojang.com/browse/MC-143768)

此方法在 Minecraft 1.17.1 及更高版本中 100% 有效。

## 如果需要继续安装

{% content-ref url="../../first-install.md" %}
[first-install.md](../../first-install.md)
{% endcontent-ref %}
