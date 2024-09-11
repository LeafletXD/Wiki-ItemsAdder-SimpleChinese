# 使用Optifine、CIT后自定义盔甲无法正常显示

## 使用Optifine、CIT后自定义盔甲无法正常显示

如果你为皮革盔甲创建了自定义 CIT，它可能无法正常显示。

要修复此问题，请确保在自定义 CIT 中添加 `weight` 属性。该属性使 Optifine 优先加载你的 CIT，从而确保它能够正确显示。

示例：

```editorconfig
type=armor
items=leather_helmet leather_chestplate leather_leggings leather_boots
texture.leather_layer_1=my_layer_1
texture.leather_layer_2=my_layer_2
nbt.display.Name=ipattern:My Custom Armor
weight=99999
```
