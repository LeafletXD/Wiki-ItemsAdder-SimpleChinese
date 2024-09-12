---
描述: 特殊文本动画和着色效果
---

# 🎆 文字效果（1.17+）

{% hint style="warning" %}
* **需要 Minecraft 1.17+ 客户端**
* 在 [Minecraft 语言文件](adding-content/minecraft-language-files.md) 中不起作用（游戏限制）
* 编辑 `rendertype_text` 着色器文件
{% endhint %}

## 什么是文本效果？

文本效果是一些酷炫的装饰性文本效果，可以用来让你的服务器看起来更专业。

{% hint style="warning" %}
你必须运行 `/iazip` 来启用/禁用此功能。\
确保在 `config.yml` 中也启用此功能。

```yaml
effects:
  text-effects:
    enabled: true # 更改此选项时需要使用 /iazip。
    customitem-name-and-lore:
      enabled: true
    chat:
      enabled: true
    sign:
      enabled: true
    book:
      enabled: true
    anvil:
      enabled: true
```
{% endhint %}

## 权限

* 在 **聊天** 中使用 **文本效果**
  * `ia.user.text_effect.chat`
* 在 **木牌** 中使用 **文本效果**
  * `ia.user.text_effect.sign`
* 在 **书籍** 中使用 **文本效果**
  * `ia.user.text_effect.book`
* 在 **铁砧** 重命名字段中使用 **文本效果**
  * `ia.user.text_effect.anvil`
* 使用 **文本效果**
  * `ia.user.text_effect.use.<effect>`

## 效果列表

### 彩虹

![](../.gitbook/assets/rainbow.gif)

![](../.gitbook/assets/image\_\(128\).png)

![](../.gitbook/assets/image\_\(129\).png)

![](../.gitbook/assets/rainbow\_item.gif)

权限: `ia.user.text_effect.use.r`\
用法: `<r text>`

### 摇摆

![](../.gitbook/assets/wobble.gif)

![](../.gitbook/assets/wobble\_item.gif)

权限: `ia.user.text_effect.use.w`\
用法: `<w text>`

### 跳跃

![](../.gitbook/assets/jump\_chat.gif)

![](../.gitbook/assets/jump.gif)

![](../.gitbook/assets/jump\_boss.gif)

权限: `ia.user.text_effect.use.j`\
用法: `<j text>`

### 彩虹 + 摇摆

![](../.gitbook/assets/rw\_chat.gif)

权限: `ia.user.text_effect.use.rw`\
用法: `<rw text>`

### 彩虹 + 跳跃

![](../.gitbook/assets/rj.gif)

权限: `ia.user.text_effect.use.rj`\
用法: `<rj text>`

## 可以在哪里使用这些效果？

* 自定义物品名称（在 .yml 文件中）
* 自定义物品描述（在 .yml 文件中）
* 聊天
* 木牌
* 书籍
* Bossbar
* 前缀-后缀（例如 Luckperms）
* _更多内容即将推出..._

![](../.gitbook/assets/rainbow\_wobble\_lore.gif)

## 如何创建动画前缀（Luckperms）

![](../.gitbook/assets/image\_\(133\).png)

`/lp group admin meta setprefix "<rw ADMIN >"`

![](../.gitbook/assets/prefix.gif)

点击这里阅读 [Luckperms 官方教程](https://luckperms.net/wiki/Prefixes,-Suffixes-&-Meta)，如果你不知道前缀是如何工作的。

## 在不使用占位符的情况下使用文本效果

如果你想在不支持 ItemsAdder 占位符的区域（如 `<r TEXT>`）中使用文本效果，可以使用另一种方法。

这些效果是基于 **特殊 HEX 颜色** 触发的。\
因此，如果你想展示文本效果的区域支持 HEX 颜色，你可以这样做。

### 特殊颜色

#### 彩虹

`#FFFFFE`

#### 摇摆

`#FFFFFD`

#### 跳跃

`#FFFFFB`

#### 彩虹 + 摇摆

`#FFFFFC`

#### 彩虹 + 跳跃

`#FFFEFE`

### 在 Minecraft 原生 JSON 表示法中使用

触发彩虹效果：\
`/tellraw @a {"text":"custom text example", "color":"#FFFFFE"}`

用你想要的效果替换 `FFFFFE`。

### 在支持 _MiniMessage_ 的插件中使用

{% embed url="https://docs.advntr.dev/minimessage/format.html#color" %}

（例如 ItemsAdder 自身和 [ChatFormatter](https://www.spigotmc.org/resources/102212/)）

触发彩虹效果：`<#FFFFFE>custom text example`

用你想要的效果替换 `FFFFFE`。

### 在支持旧版 HEX 表示法的插件中使用

#### 彩虹

`&X&F&F&F&F&F&E`

#### 摇摆

`&X&F&F&F&F&F&D`

#### 跳跃

`&X&F&F&F&F&F&B`

#### 彩虹 + 摇摆

`&X&F&F&F&F&F&C`

#### 彩虹 + 跳跃

`&X&F&F&F&F&F&E`

此方法已在 [EpicRename](https://www.spigotmc.org/resources/epicrename.4341/) 上测试，应该可以在 Spigot 使用其旧版颜色代码的任何插件或地方中工作。

示例：`/rename &x&F&F&F&F&F&ETest`
