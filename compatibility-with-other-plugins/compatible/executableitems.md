# ExecutableItems

## [下载地址](https://www.spigotmc.org/resources/custom-items-free-executable-items-1-12-1-17.77578/)

## 如何将 ExecutableItem 连接到 ItemsAdder 自定义物品

{% hint style="warning" %}
更新 **ITEMSADDER** 至 **2.2.20 及以上**\
更新 **ExecutableItems** 至 **4.2.3.5 及以上**
{% endhint %}

## 创建 ItemsAdder 物品

### 创建你的 .yml 文件并添加所有 ItemsAdder 物品的属性

在这个例子中，我将把一个名为 `executableitem_test` 的 **ItemsAdder** 物品连接到 ExecutableItems 示例文件中的 `spit` 物品。

```yaml
info:
  namespace: example
items:
  executableitem_test:
    display_name: executableitem_test
    permission: executableitem_test
    executableitem:
      id: Free_Spit
    resource:
      material: IRON_INGOT
      generate: true
      textures:
      - item/executableitem_test.png
    durability:
      max_custom_durability: 1324
```

{% hint style="success" %}
如你所见，我设置了一个新的属性叫做 **`executableitem`** 和 **`id`**。\
这些属性用于 **连接** **两个物品**。
{% endhint %}

### 获取物品

运行 `/iaget executableitem_test` 来获取这个物品！

![](<../../.gitbook/assets/image\_(140) (1) (1).png>)
