# 无法在家具上放置物品展示框

{% embed url="https://github.com/PluginBugs/Issues-ItemsAdder/issues/1913" %}

这是一种 Minecraft 的行为，游戏会强制移除物品展示框，因为它处于另一个实体之内，在这种情况下是家具物品展示框。

### 解决方案

将家具物品展示框的高度减少 `0.1`。\
例如，将 `1` 调整为 `0.9`，将 `2` 调整为 `1.9` 等等。

```yaml
        hitbox:
          length: 1
          width: 1
          height: 1.9
```
