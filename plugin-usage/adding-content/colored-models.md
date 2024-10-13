# 🎨 彩色模型

{% hint style="info" %}
如果你想制作彩色的元素（例如自定义的彩色家具或彩色的车辆），你无需为每个不同颜色的物品制作单独的模型。
{% endhint %}

## 我该怎么做？

### 1. 用 Blockbench 打开你的模型

![](../../.gitbook/assets/image\_\(79\).png)

### 2. 选择你想要上色的面

![](../../.gitbook/assets/image\_\(80\).png)

### 3. 使用白色/灰色的纹理，以获得更好的上色效果

### 4. 启用隐藏的 "Tint" 功能

![](../../.gitbook/assets/image\_\(81\).png)

![](../../.gitbook/assets/image\_\(83\).png)

### 5. 启用你希望着色的面

![](../../.gitbook/assets/image\_\(85\).png)

### 6. 在你的 .yml 文件中设置特定的颜色属性。

在这个例子中，我使用了 `leather_horse_armor`，但你也可以使用 `potion`。

```yaml
  orange_modern_lamp:
    display_name: "Orange Modern Lamp"
    specific_properties:
      leather_horse_armor:
        color: ORANGE
    resource:
      material: LEATHER_HORSE_ARMOR
      generate: false
      model_path: item/template_modern_lamp
```

{% hint style="info" %}
如果你想使用特定的颜色，你可以使用 [这个颜色选择器](https://www.mathsisfun.com/hexadecimal-decimal-colors.html)。\
复制 **十进制** 颜色（十六进制）。
{% endhint %}

### 7. 现在你可以创建任意数量的家具，只需更改颜色，游戏会自动对其进行着色

![](../../.gitbook/assets/image\_\(86\).png)
