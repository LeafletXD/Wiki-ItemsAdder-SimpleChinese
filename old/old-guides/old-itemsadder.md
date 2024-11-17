---
描述: ItemsAdder 3.3.0 之前的版本
---

# 🗑 删除默认内容 v3.2

## ItemsAdder 3.3.0 之前的版本

{% hint style="warning" %}
仅当你使用的是旧版 ItemsAdder 资源包时阅读此内容。\
如果你是在 v3.2.0 或之后购买的插件，可以忽略此内容。
{% endhint %}

## 如何移除所有物品和默认内容？

{% hint style="info" %}
如果你不需要默认内容，只想创建自己的物品、方块和其他内容，这很简单！\
请按照以下教程操作。
{% endhint %}

### 1. Config.yml

打开插件的 `config.yml` 文件，并将以下设置为 **false**。

```yaml
  extract-default-items: false
  extract-default-resources: false
```

### 2. 删除你不需要的文件夹。可以从以下列表中选择。

#### Twitter 表情符号

`plugins\ItemsAdder\data\items_packs\twitteremojis`\
`plugins\ItemsAdder\data\resource_pack\assets\twitteremojis`

#### Magic Craft 示例

`plugins\ItemsAdder\data\items_packs\magiccraft`\
`plugins\ItemsAdder\data\resource_pack\assets\magiccraft`

#### Minecraft 表情符号

`plugins\ItemsAdder\data\items_packs\mcemojis`\
`plugins\ItemsAdder\data\resource_pack\assets\mcemojis`

#### ItemsAdder 项目

`plugins\ItemsAdder\data\items_packs\itemsadder`\
`plugins\ItemsAdder\data\resource_pack\assets\itemsadder`

#### 示例项目

`plugins\ItemsAdder\data\items_packs\example`\
`plugins\ItemsAdder\data\resource_pack\assets\example`

### 3. 完成更改

运行以下命令：`/iacleancache items`

删除这些文件夹：\
`ItemsAdder\storage\cache\tmp\` `ItemsAdder\data\resource_pack\assets\minecraft\models\item\` `ItemsAdder\data\resource_pack\assets\minecraft\blockstates\`

然后运行 `/iazip`

{% hint style="danger" %}
#### 请勿删除列表中未列出的其他文件夹。

如果你删除了 minecraft、mcguis 或 mcicons 文件夹，插件的某些部分可能会停止工作。
{% endhint %}
