# DecentHolograms

## [点击下载](https://www.spigotmc.org/resources/96927/)

## 如何显示自定义物品？

- 运行 `/iacustommodeldata <item>`（例如：`/iacustommodeldata ruby`）
- 记住自定义物品的基础物品和 `CustomModelData`（例如：`IRON_INGOT` 和 `10000`）
- 使用 `/dh create <name> [Line]` 创建一个新的全息图（如果你已经有悬浮字，则可以跳过此步骤）
- 使用 `/dh l add <name> <page> #ICON: <item> {CustomModelData: <cmd>}` 将物品添加到悬浮字中（例如：`/dh l add example 1 #ICON: IRON_INGOT {CustomModelData: 10000}`）

{% hint style="success" %}
在创建悬浮字时，可以将 `#ICON: <item> {CustomModelData: <cmd>}` 作为 `/dh create` 的第一行。  
示例：`/dh create example #ICON: IRON_INGOT {CustomModelData: 10000}`
{% endhint %}
