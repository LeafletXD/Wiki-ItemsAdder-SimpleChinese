---
描述： ItemsAdder 兼容 MMOItems，并且非常容易整合
---

# MMOItems

**下载** [MMOItems](https://www.spigotmc.org/resources/mmoitems-premium.39267/)

### 这里可以下载本教程中展示的示例包

{% embed url="https://www.spigotmc.org/resources/items-mmoitem-example-integration.88351/" %}

## 已知限制

{% embed url="https://github.com/PluginBugs/Issues-ItemsAdder/issues/2008" %}

## 将 MMOItem 连接到 ItemsAdder 物品

### 使用命令 /mmoitems browse

![](<../../../.gitbook/assets/image_(25).png>)

### 创建新的 MMOItem

![](<../../../.gitbook/assets/image_(26).png>)

![](<../../../.gitbook/assets/image_(29).png>)

### 添加所有你想要的属性，例如魔法伤害等

![](<../../../.gitbook/assets/image_(28).png>)

### 在 /mmoitems browse 中预览 MMOItem

![](<../../../.gitbook/assets/image_(30).png>)

### 按照通常的方式创建你的 .yml 文件，并添加所有 ItemsAdder 物品的属性

`ItemsAdder/contents/mmoitems_example/configs/example.yml`

{% hint style="success" %}
如你所见，我设置了一个新的属性叫做 **`mmoitem`** 以及 **`type`** 和 **`id`**。\
这些用于 **连接** **两个物品**。
{% endhint %}

```yaml
info:
  namespace: mmoitems_example
items:
  test:
    display_name: ""
    permission: example_item
    mmoitem:
      type: SWORD
      id: TEST
    resource:
      material: DIAMOND_SWORD
      generate: true
      textures:
      - item/test.png
    durability:
      max_custom_durability: 1324
```

### 按照通常的方式创建你的 .png 纹理

`ItemsAdder/contents/mmoitems_example/resourcepack/mmoitems_example/textures/item/test.png`

### 获取物品

使用命令 `/iaget mmoitems_example:test` 来获取你完成的物品

![](<../../../.gitbook/assets/image_(33).png>)

![](<../../../.gitbook/assets/image_(34).png>)
