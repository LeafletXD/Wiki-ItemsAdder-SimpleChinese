---
描述: 在某些区域/自定义世界中出现的方块故障
---

# 地图里的方块出现故障

## 方块故障

{% hint style="info" %}
如果你使用 `REAL` 或 `REAL_TRANSPARENT` 类型来创建自定义方块，这种情况是正常的。  
ItemsAdder 使用蘑菇方块和紫颂植物来创建这些方块。

这是因为游戏在游戏过程中生成这些方块，以创建一些结构（例如：在主世界中生成的大蘑菇和末地的紫颂植物），因此它们可能会带有一些特定的方块数据，这会与 ItemsAdder 方块产生冲突。
{% endhint %}

{% hint style="success" %}
这只是一个图形故障，这种状态不会导致重复错误或类似问题。
{% endhint %}

![](<../../../.gitbook/assets/image (50) (1) (1) (1).png>)

通常你应该避免使用 `REAL` 自定义方块类型（蘑菇），而使用 `REAL_NOTE` 自定义方块类型。  
`REAL_NOTE` 使用 **音符盒** 来创建自定义方块，因此你不会遇到这种问题，因为音符盒不会在原版世界中自然生成。

## 如何修复

打开 `config.yml` 并设置以下选项：

{% code title="config.yml" %}
```yaml
  fix-glitched-blocks:
    enabled: true
    only-new-chunks: false
```
{% endcode %}

## Paper 1.20.1+ 高级修复

### 禁用 REAL_NOTE 方块的故障

```yaml
block-updates:
  disable-noteblock-updates: true
  disable-tripwire-updates: true
```

{% hint style="warning" %}
### 注意

设置 `disable-tripwire-updates: true` 将完全停止 tripwire 的更新。  
这可能导致 tripwire 触发器无法再正常工作。

设置 `disable-noteblock-updates: true` 也会造成相同的行为。  
这意味着 NO 更新，因此你将无法使用音乐红石电路。
{% endhint %}

## Purpur（1.20.1 之前）高级修复

{% hint style="warning" %}
**仅适用于** [**Purpur**](https://purpur.pl3x.net)**。**  
**Spigot** 和 **Paper** 没有此功能。
{% endhint %}

在 **`purpur.yml`** 配置中启用以下选项：

* [https://purpurmc.org/docs/Configuration/disable-mushroom-updates](https://purpurmc.org/docs/Configuration/disable-mushroom-updates)
* [https://purpurmc.org/docs/Configuration/disable-note-block-updates](https://purpurmc.org/docs/Configuration/disable-note-block-updates)
* [https://purpurmc.org/docs/Configuration/disable-chorus-plant-updates](https://purpurmc.org/docs/Configuration/disable-chorus-plant-updates)

{% hint style="warning" %}
注意：`disable-chorus-plant-updates: true` 将完全停止紫颂植物的更新。因此，当第一个方块被破坏时，你将不会看到链条断裂的效果。
{% endhint %}

**示例：**

```yaml
  blocks:
    disable-mushroom-updates: true
    disable-note-block-updates: true
    disable-chorus-plant-updates: true
```
