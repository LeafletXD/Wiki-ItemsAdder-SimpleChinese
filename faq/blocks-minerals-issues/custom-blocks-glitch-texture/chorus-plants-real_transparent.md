# 紫颂植物 (REAL_TRANSPARENT)

## REAL_TRANSPARENT 方块在某些情况下的破坏动画问题

{% embed url="https://youtu.be/1HPjKn_vmw8" %}

{% hint style="info" %}
这并不会造成严重问题，你可以忽略它！
{% endhint %}

这只是一个图形故障，不能在普通的 **Spigot** 或 **Paper** 中修复。  
如果你想完全修复它，你需要安装 **Purpur** 并在其 `purpur.yml` 文件中设置此选项。

{% hint style="warning" %}
**仅适用于** [**Purpur**](https://purpur.pl3x.net)**。**  
**Spigot** 和 **Paper** 没有此功能。

这将完全停止紫颂植物的更新。因此，当第一个方块被破坏时，你将不会看到链条断裂的效果。

[更多信息请参阅](https://purpurmc.org/docs/Configuration/disable-chorus-plant-updates)
{% endhint %}

```yaml
  blocks:
    disable-chorus-plant-updates: true
```

### 自动掉落拾取重复问题

如果你有一个自动掉落拾取插件，你可能会遇到当紫颂植物出现图形故障时，紫颂果会随机添加到你的背包中的问题。

要修复此问题，你需要移除自动掉落拾取插件，或者请求其开发者添加一个选项，以禁用自动拾取某些物品（紫颂果）或某些方块（紫颂植物）。
