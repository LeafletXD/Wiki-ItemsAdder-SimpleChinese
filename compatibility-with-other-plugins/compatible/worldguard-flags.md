---
描述： Worldguard flags列表
---

# WorldGuard

## Flags列表

### ia-furniture-sit

此标志允许玩家坐在家具上（家具具有 `furniture_sit` [行为](../../plugin-usage/adding-content/item-properties/behaviours.md)）。

### ia-campfire-item-add

允许用户将物品移到篝火上。

### ia-campfire-item-remove

允许用户从篝火上移除物品。

### ia-vehicle-place

允许用户在区域内放置车辆。

### ia-vehicle-remove

允许用户移除区域内的任何车辆。

### ia-vehicle-personal-remove

允许用户仅移除他们自己的车辆。

### ia-vehicle-sit

允许用户坐在区域内的任何车辆上。

### ia-vehicle-personal-sit

允许用户仅坐在他们自己的车辆上。

### ia-trade-machine-use

允许用户使用交易机器。

### ia-placed-block-interact

允许用户触发 `placed_block.interact` 事件。

### ia-placed-armorstand-interact

允许用户触发 `placed_armorstand.interact` 事件。

{% hint style="info" %}
将 **ia-vehicle-sit** 设置为拒绝，将 **ia-vehicle-personal-sit** 设置为允许，以便玩家只能坐在个人车辆上。
{% endhint %}

## 常见问题

{% hint style="warning" %}
如果用户即使设置了正确的标志仍然**不能坐**在**家具**上：

* 检查是否正在使用 `__global__` 区域作为主要区域（即应用了家具标志的区域）。如果是，请创建一个新的区域。全局区域已知在某些插件Flags上存在问题。
* 检查是否设置了 `build` 或 `passthrough` Flags。\
  请记住，这些Flags不能更改，应保持默认值（未选中，灰色文本）。
{% endhint %}
