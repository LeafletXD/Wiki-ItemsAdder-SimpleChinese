---
description: 如何使用外部托管与 IA
---

# 📤 自动外部托管

{% hint style="warning" %}
## 本指南已过时，将不再有效

PloudOS 正在关闭，遗憾的是，我没有控制权，因为我不拥有该业务。

请使用其他托管方法，因为这个将不再有效。
{% endhint %}

## 视频教程

{% embed url="https://www.youtube.com/watch?v=fOpB5-80coY" %}

## 什么是自动托管？

**ItemsAdder** 允许您将资源包自动上传到 **全球各地的免费在线服务** 上。

非常感谢 [PloudOS](https://ploudos.com/it/) 提供他们的平台，让我可以免费托管您的资源包！

{% embed url="https://ploudos.com/" %}

## 有什么优势？

主要优势是下载速度和可用性。\
此服务允许您的玩家快速下载资源包，不论他们身处哪个国家（基于云的平台）。

## 我已经使用自托管，这个更好吗？

根据情况而定。\
如果您正在处理资源包，并且需要不断运行 `/iazip`，以避免浪费时间，建议使用 [自托管](../../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md)（详细信息请阅读 [这里](../../plugin-usage/resourcepack-hosting/tips-for-fastest-usage.md)）。

当您完成资源包的工作后，可以安全地开始使用 `auto-external-host` 功能。\
这将使您的服务器流量降低，因为资源包将不再托管在您的服务器上。

如果您的玩家群体都来自同一个国家，您可以继续使用 `自托管`。

## 如何使用？

您只需：

* 在 `config.yml` 中启用 `auto-external-host`
* 禁用所有其他托管方法。

```yaml
auto-external-host:
  enabled: true
```

### 最后一步

运行 `/iazip` 以 **压缩** 资源包。\
**插件** 将 **自动上传** 它到网上（您仅需在第一次使用时 **接受隐私政策**）。

**完成了！** 没有其他操作，享受您的 **免费自动化资源包托管**。

## 我的资源包会被随机人群访问吗？

2021-08-16：\
您的资源包不会被 Google 索引，也不会出现在资源包列表中。\
只有知道链接的人才能下载该包。

## 如果需要，请继续安装步骤

{% content-ref url="../../first-install.md" %}
[首次安装](../../first-install.md)
{% endcontent-ref %}
