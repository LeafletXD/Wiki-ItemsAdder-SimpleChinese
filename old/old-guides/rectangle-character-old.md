# ▯ 矩形字符 - 旧版

## 卸载 Custom ESC 插件后我看到 ▯ 字符

{% hint style="info" %}
此问题仅发生在 ItemsAdder 3.3.0 之前的版本。
{% endhint %}

{% hint style="info" %}
卸载 [Custom ESC 插件](https://www.spigotmc.org/resources/addon-custom-esc-menu-and-death-screen-for-itemsadder.88809/) 时，此方法有用。
{% endhint %}

您需要删除以下文件夹：`data/resource_pack/assets/minecraft/lang`

然后运行 `/iazip` 命令。

![](<../../.gitbook/assets/image\_(140) (1).png>)

## 1.19 客户端显示 ☐ 代替某些字体图像

这是由一个 Minecraft 无法修复的 bug 引起的：[https://bugs.mojang.com/browse/MC-253169](https://bugs.mojang.com/browse/MC-253169)

Reddit 讨论帖：[https://www.reddit.com/r/Mojira/comments/vis77z/mc253169\_bug\_report\_marked\_as\_resolved\_but\_its/](https://www.reddit.com/r/Mojira/comments/vis77z/mc253169\_bug\_report\_marked\_as\_resolved\_but\_its/)

### 如何修复？

修复很简单：您只需打开 **客户端** 日志（不是服务器日志），并找到显示字体加载错误的日志，该错误导致其他字体图像无法加载：[阅读客户端日志](../../faq/identify-why-textures-are-not-shown.md)。

您可能有一个或多个配置错误的图像，这些图像是导致此问题的根本原因。

#### 配置错误的 PNG 示例：

以下示例包包含一个 `height` 高于 `y_position` 的 PNG 图像。

```
Unable to load font 'minecraft:default' in fonts.json in resourcepack: '260e803a4ce18a1662a5ff9c59f9d758ab1026bb'
com.google.gson.JsonParseException: Ascent 30 higher than height 9
	at net.minecraft.class_386$class_387.method_2037(class_386.java:74)
```
