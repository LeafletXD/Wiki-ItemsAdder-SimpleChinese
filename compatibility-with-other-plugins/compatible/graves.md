# Graves

## [点击下载](https://www.spigotmc.org/resources/graves.74208/)

## 如何添加兼容性？

启用兼容性设置

```yaml
itemsadder: # https://www.spigotmc.org/resources/itemsadder.73355/
  enabled: true # 是否启用 ItemsAdder 集成
```

编辑默认选项。如果需要，您也可以自定义物品（确保它们是正确的类型，使用家具时在家具属性中，使用块时在块属性中）。

```yaml
  ##############
  # ItemsAdder #
  ##############
  # 该选项需要 ItemsAdder，您必须安装它才能使用模型。
  itemsadder:
    furniture:
      enabled: true # 是否使用 ItemsAdder 家具？
      name: "itemsadder:mysterious_stone" # 家具名称
    block:
      enabled: true # 是否使用 ItemsAdder 块？
      name: "itemsadder:nice_stone" # 块名称
```
