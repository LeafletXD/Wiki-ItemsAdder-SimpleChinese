---
描述：使用另一种 .json 文件生成自定义字体图像
---

# 替代字体文件

## 如何使用替代自定义字体文件

{% hint style="danger" %}
**此功能不稳定，已从插件中移除。目前无法使用。**
{% endhint %}

**ItemsAdder** 为您的自定义 **font_images** 生成 json 文件，在某些情况下，您可能希望使用一个单独的文件，而不是将图像追加到 `default.json` 中。

如果配置了，ItemsAdder 将在新文件 `assets/minecraft/font/custom.json` 中生成 **font_images**，而不是在 `default.json` 中。

## 为什么要使用单独的自定义字体文件？

这样可以使您的 font_images 使用完全独立的字体，而不会覆盖主字体字符。

Minecraft 1.16+ 具有原生自定义字体功能，可以在每条消息中指定字体名称（使用 json）。

例如，您可以输入以下命令 `/tellraw @a [{"text":"测试消息！","font":"default"},"\n",{"text":"测试消息！","font":"alt"}]`

该命令将使用 `default` 字体显示第一条文本，使用 `alt` 字体显示第二条文本（在这种情况下，它已包含在游戏中）。

![](../../.gitbook/assets/image\_\(153\).png)

ItemsAdder 自定义字体将命名为 `custom`，因此在这种情况下，您需要使用属性 `"font":"custom"`。

## 缺点和优点

{% hint style="danger" %}
* 表情符号不会显示在 `/e` 自动完成命令中，而是显示占位符 ([截图](https://i.imgur.com/Im9AXae.png))
* 无法在任何地方复制和粘贴 Unicode 字符，您必须依赖 `:XXX:` 和 `%img_XXX%` 占位符，或者在原版 json 组件中指定 `font` 属性（请查看 [示例](alternative-font-file.md#why-having-a-separate-custom-font-file)）
* 仅在 Minecraft 1.16+ 上可用
* **config.yml** 中的一些设置将不再有效：
  * `font_images.command`
  * `font_images.scoreboard-teams`
  * `font_images.vault-prefix-suffix`
  * `font_images.player-display-name` <mark style="color:orange;">（仅在 Paper 上有效）</mark>
  * 广播消息中的图像 <mark style="color:orange;">（仅在 Paper 上有效）</mark>
  * 牌子、书 <mark style="color:orange;">（仅在 Paper 上有效）</mark>
{% endhint %}

{% hint style="success" %}
* 玩家可以设置 `Force Unicode: On`，**font_images** 仍会显示，因为它们使用的是另一种字体，而不是默认字体。
{% endhint %}

## 我应该使用此功能吗？

{% hint style="danger" %}
**此功能不稳定**

我建议避免使用此功能，因为它有太多缺点。但我会让您自行决定，因为某些服务器可能需要将自定义图像与默认字体分开。
{% endhint %}

## 如何启用此功能？

您需要在 `config.yml` 中启用此选项并运行 `/iazip`：

{% code title="config.yml" %}
```yaml
zip:
  use_separate_custom_font_file_EXPERIMENTAL: true
```
{% endcode %}

##
