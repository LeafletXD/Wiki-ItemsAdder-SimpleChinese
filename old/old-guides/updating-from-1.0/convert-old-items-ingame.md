# 游戏内转换旧物品/方块

{% hint style="danger" %}
**建议创建一个全新的世界，不要使用旧世界，尽管转换工具可以工作，但它们仍处于实验阶段。**
{% endhint %}

{% hint style="danger" %}
这些功能**可能会导致卡顿**，建议仅启用几天，然后关闭它们以避免不必要的延迟。
{% endhint %}

## 如何自动转换世界中的旧物品

当您从 ItemsAdder 1.0 更新到 2.0 时，您可能会发现大多数物品已经更改，因此它们与更新前的旧物品不同。\
因此，我开发了一个功能，可以自动将旧物品替换为新物品。每当玩家在世界中打开一个容器（如箱子、容器等，但**不包括他们自己的背包**）时，此过程会自动运行。

要启用此功能，您需要在 **ItemsAdder 2.0** 的 `converter.yml` 文件中，将以下属性设置为 `true`。

#### 确保 `inventory-open` 被设置为 `true`：

```
items-auto-update:
  debug: false
  inventory-open: true
```

## 如何自动转换世界中放置的旧方块

您需要打开 `converter.yml` 文件，并将您自定义的旧方块的 **model_id** 映射到 IA 2.0 的新 **namespaced** 方块。例如，我已经添加了旧的 ItemsAdder 1.0 方块映射，以便将它们转换为 2.0 的命名空间方块。

### 确保将 `enabled` 设置为 `true`：

```
blocks:
  enabled: true
  debug: false
  conversion-map:
    "1": "itemsadder:ruby_block"
    "2": "itemsadder:crystal_block"
    "3": "itemsadder:spinel_block"
    "4": "itemsadder:turquoise_block"
    "5": "itemsadder:aqua_aura_block"
    "6": "itemsadder:amethyst_block"
    "7": "itemsadder:amethyst_prism_block"
    "8": "itemsadder:crying_obsidian"
    "9": "itemsadder:nice_stone"
    "10": "itemsadder:nice_wood"
    "11": "itemsadder:modern_stone"
    "12": "itemsadder:modern_sandstone"
    "13": "itemsadder:modern_quartz"
    "14": "itemsadder:ruby_ore"
    "15": "itemsadder:spinel_ore"
    "16": "itemsadder:turquoise_ore"
    "17": "itemsadder:aqua_aura_ore"
    "18": "itemsadder:amethyst_ore"
    "19": "itemsadder:bronze_ore"
    "20": "itemsadder:mysterious_ore"
    "21": "itemsadder:end_ore"
    "22": "itemsadder:restoration_table"
    "23": "itemsadder:customization_table"
    "24": "itemsadder:iron_dirt_ore"
    "25": "itemsadder:gold_dirt_ore"
    "26": "itemsadder:coal_dirt_ore"
    "27": "itemsadder:blaze_powder_ore"
    "28": "itemsadder:nether_alchemy_ore"
```
