# 在游戏中转换旧物品/方块

{% hint style="danger" %}
**建议启动一个全新的世界，不要使用旧世界，因为转换器虽然有效，但仍处于实验阶段。**
{% endhint %}

{% hint style="danger" %}
这些功能可能会导致延迟，请仅在几天内启用它们，然后禁用以避免不必要的延迟。
{% endhint %}

## 如何在您的世界中自动转换旧物品

当您从 ItemsAdder 1.0 更新到 2.0 时，您会发现大多数物品已发生变化，因此它们与更新前的旧物品不同。\
因此，我必须编写一个功能来自动替换旧物品为新物品。此过程会在每次玩家打开世界中的库存时运行（如箱子、容器等，但不是他们自己的库存）。

为了启用此功能，您需要在 **ItemsAdder 2.0** 的 `converter.yml` 文件中将以下属性设置为 `true`。

#### 确保将 `inventory-open` 设置为 `true`

```
items-auto-update:
  debug: false
  inventory-open: true
```

## 如何自动转换世界中已放置的旧方块

您需要打开 `converter.yml` 文件，并将您自己的旧方块 **model_id** 映射到 IA 2.0 的新 **namespaced** 方块。例如，我已经添加了旧 ItemsAdder 1.0 方块的映射，以将其转换为 2.0 的命名空间方块。

#### 确保已设置 enabled: true

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
