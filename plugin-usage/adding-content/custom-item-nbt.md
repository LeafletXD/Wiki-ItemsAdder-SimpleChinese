# 📎 自定义物品 NBT 标签

## 为物品添加自定义 NBT 属性

你可以为自定义物品指定自定义 **NBT** 属性，并将其合并到物品中。

{% hint style="danger" %}
请确保提供有效的 **NBT** (`json`) 格式，否则它将不起作用！
{% endhint %}

{% hint style="warning" %}
确保使用 `\` 转义 `"` 字符。
{% endhint %}

{% hint style="success" %}
此功能支持旧版 NBT 和 1.20.5+ 的新版 NBT！\
如果需要，它会自动转换旧版 NBT。

点击查看关于 [1.20.5+](https://www.minecraft.net/en-us/article/minecraft-java-edition-1-20-5) 更改的更多信息（向下滚动查看）。
{% endhint %}

### 自定义属性示例

例如，我想将以下标签合并到我的物品中：\
`{my-custom-nbt-tag:"hello this is a custom tag", another-tag:"useless"}`

```yaml
items:
  custom_nbt_item:
    display_name: "Just an example"
    permission: examples.custom_nbt_item
    nbt: '{my-custom-nbt-tag:"hello this is a custom tag", another-tag:"useless"}'
    resource:
      material: DIAMOND_SWORD
      generate: true
      model_path: "minecraft:item/diamond"
    durability:
      max_custom_durability: 1324
```

### 自定义物品名称示例

```yaml
items:
  example_item_custom_name:
    enabled: true
    display_name: example_item_custom_name
    permission: custom.example_item_custom_name
    nbt: "{display:{Name:'{\"text\":\"TEST\", \"font\": \"alt\"}'}}"
```

<figure><img src="../../.gitbook/assets/nbt_custom_item_name_example.png" alt=""><figcaption></figcaption></figure>
