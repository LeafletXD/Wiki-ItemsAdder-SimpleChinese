# 🎁 掉落物

掉落物用于指定何时掉落特定物品。

您可以决定创建不同的掉落类型：

* 方块
* 生物
* 钓鱼

例如，这是我创建的 `.yml` 文件的掉落物类别。

{% hint style="warning" %}
<mark style="color:red;">不要忘记命名空间！</mark>\
不要忘记为每个配置定义命名空间！
{% endhint %}

```yaml
info:
  namespace: my_loots
loots:
  blocks:
    ruby_ore:
      type: iasurvival:ruby_ore
      items:
        ruby:
          item: iasurvival:ruby
          min_amount: 1
          max_amount: 2
          chance: 100
    nether_quartz_ore:
      type: NETHER_QUARTZ_ORE
      drop_only_first: true
      items:
        crystal:
          item: iasurvival:crystal
          min_amount: 1
          max_amount: 2
          chance: 10
        knowledge_fragment:
          item: iasurvival:knowledge_fragment
          min_amount: 1
          max_amount: 2
          chance: 15
```

这个示例在 **方块** 类别中有两个掉落物。

第一个叫 `ruby_ore`（您可以根据自己的喜好命名），当您破坏类型为 `iasurvival:ruby_ore` 的自定义 **方块** 时，将掉落一个 `itemsadder:ruby` 物品，最小 **数量** 为 **1**，最大数量为 **2**，且掉落 **几率** 为 **100%**。

第二个是来自一个原版 **方块** 的掉落物。可以想象，当玩家破坏 `NETHER_QUARTZ_ORE` 时，它将掉落一个 `crystal` 或 `knowledge_fragment`。\
这些 **掉落** 是由 **ItemsAdder** 根据您设置的 **几率** 决定的。

{% hint style="info" %}
特殊属性：`drop_only_first`\
这允许您 **停止** **插件** 在提取 **正确** 几率时 **掉落** 每个 **物品**。

<mark style="color:orange;">**警告**</mark><mark style="color:orange;">：这会使您的物品</mark> <mark style="color:orange;">**更难**</mark> <mark style="color:orange;">被</mark> <mark style="color:orange;">**掉落**</mark><mark style="color:orange;">。</mark>
{% endhint %}

## 仅在特定生物群落中生成

```yaml
loots:
  blocks:
    ruby_ore:
      type: iasurvival:ruby_ore
      biomes:
        - PLAINS
        - SUNFLOWER_PLAINS
        - MOUNTAINS
      items:
        ruby:
          item: iasurvival:ruby
          min_amount: 1
          max_amount: 2
          chance: 100
```

## 忽略时运附魔

您可以通过添加 `ignore_fortune` 属性来使掉落物忽略时运附魔。

```yaml
loots:
  blocks:
    ruby_ore:
      type: iasurvival:ruby_ore
      items:
        ruby:
          item: iasurvival:ruby
          min_amount: 1
          max_amount: 2
          chance: 100
          ignore_fortune: true # <----- 在这里
```

## 其他类型的掉落物

正如我之前所说，还有其他类型的掉落物：生物和钓鱼。\
以下是一些示例：

### 钓鱼

```yaml
loots:
  fishing:
    loot_blue_parrotfish:
      biomes:
        - WARM_OCEAN
      items:
        item_1:
          item: iasurvival:blue_parrotfish
          min_amount: 1
          max_amount: 1
          chance: 5
    loot_green_sunfish:
      items:
        item_1:
          item: iasurvival:green_sunfish
          min_amount: 1
          max_amount: 1
          chance: 5
    loot_goldfish:
      items:
        item_1:
          item: iasurvival:goldfish
          min_amount: 1
          max_amount: 1
          chance: 5
```

### 生物

```yaml
loots:
  mobs:
    villager:
      type: VILLAGER
      ignore_spawner: true
      nbt:
        profession:
          path: VillagerData.profession
          value: minecraft:farmer
          type: string
      items:
        item_1:
          item: iawearables:straw_hat
          min_amount: 1
          max_amount: 1
          chance: 100
    ender_dragon:
      type: ENDER_DRAGON
      items:
        item_1:
          item: iawearables:ender_dragon_wings
          min_amount: 1
          max_amount: 1
          chance: 100
```

### **自定义生物掉落物（**[**旧实体方法**](mobs/old-method/)**）**

为了让 ItemsAdder 根据您击杀自定义生物（通过 ItemsAdder 创建）掉落物品，您必须使用 `ItemsAdderMob` 元数据属性。示例：

```yaml
loots:
  mobs:
    soul:
      type: HUSK
      metadata:
        ItemsAdderMob:
          name: "ItemsAdderMob"
          value: "creaturesplus:soul"
          type: "string"
      items:
        ruby:
          item: ruby
          min_amount: 1
          max_amount: 1
          chance: 100
```

如您所见，我设置了 `ItemsAdderMob` 属性并指定了我的自定义生物的 **命名空间：ID**（在此示例中，我使用了 **creaturesplus:soul** 生物）。

### **自定义实体掉落物**

为了让 ItemsAdder 根据您击杀自定义实体（通过 ItemsAdder 创建）掉落物品，您必须使用 `ItemsAdderEntity` 元数据属性。示例：

```yaml
loots:
  mobs:
    soul:
      type: HUSK
      metadata:
        ItemsAdderEntity:
          name: "ItemsAdderEntity"
          value: "custom:ninja_skeleton"
          type: "string"
      items:
        ruby:
          item: ruby
          min_amount: 1
          max_amount: 1
          chance: 100
```

如您所见，我设置了 `ItemsAdderEntity` 属性并指定了我的自定义生物的 **命名空间：ID**（在此示例中，我使用了 **custom:ninja_skeleton** 生物）。

### **村民职业（以及您想匹配的任何其他 NBT 属性）**

```yaml
loots:
  mobs:
    villager:
      type: VILLAGER
      nbt:
        profession:
          path: VillagerData.profession
          value: minecraft:farmer
          type: string
      items:
        item_1:
          item: itemsadder:straw_hat
          min_amount: 1
          max_amount: 1
          chance: 100
```

如您所见，我设置了 **职业** 属性并指定了 **NBT 属性** 路径，在这种情况下是 **VillagerData.profession**。\
然后我将值设置为 **minecraft:farmer**，这告诉 ItemsAdder 仅匹配属性 **VillagerData.profession** 设置为 **minecraft:farmer** 的 **村民**。

{% hint style="warning" %}
**nbt** 和 **metadata** 的类型属性非常 **重要**，不要 **忘记** 它们，否则匹配可能无法发生。
{% endhint %}

### **基于方块实体 NBT 数据掉落（例如刷怪蛋）**

```yaml
loots:
  blocks:
    change_me:
      enabled: true
      type: SPAWNER
      nbt:
        spawner_type:
          path: SpawnData.entity.id
          value: minecraft:zombie
          type: string
      items:
        change_me:
          item: ACACIA_BOAT
          min_amount: 1
          max_amount: 1
          chance: 100
          ignore_fortune: false
```

{% hint style="warning" %}
如果您希望通过使用附魔物品（带有丝触）从刷怪蛋中获取物品，则必须启用此设置。

```yaml
loots:  
    allow-loots-drop-from-spawners-using-silk-touch: true
```
{% endhint %}

## 每个世界的掉落物

{% hint style="warning" %}
这需要 ItemsAdder 3.2.5 及以上版本
{% endhint %}

```yaml
loots:
  blocks:
    change_me:
      enabled: true
      type: SAND
      biomes:
        - BEACH
      worlds:
        - "world_*"
        - "!private_*"
        - "example1"
        - "!example2"
      items:
        change_me:
         

 item: STONE
          min_amount: 1
          max_amount: 1
          chance: 100
          ignore_fortune: false
```

如果您没有指定任何世界，掉落物将在所有世界中掉落。

特殊的 `*` 字符允许任何以特定文本开头的世界。\
在此示例中，每个以 `world_` 开头的世界都将匹配并掉落掉落物。

特殊的 `!` 字符拒绝在任何以特定文本开头的世界中掉落。\
在此示例中，每个以 `private_` 开头的世界都将匹配并不允许掉落物。

您还可以指定精确的世界名称，在此示例中，`example2` 将不允许掉落物掉落。

您还可以指定精确的世界名称，在此示例中，`example1` 将允许掉落物掉落。

## 带特定皮肤的 `PLAYER_HEAD` 掉落

如何分配带纹理的 `PLAYER_HEAD` 作为掉落物。

### 准备头部掉落（唯一现有的解决方法）

为要掉落的玩家头部创建一个新的自定义物品。

1. 创建一个新文件（我命名为 `playerheads.yml`），在其中设置 `nbt` 以设置可以在 [minecraft-heads.com](https://minecraft-heads.com) 找到的纹理。

    {% hint style="warning" %}
    `skull` 可以设置为您想要的任何值
    {% endhint %}
2. 材料必须为 `PLAYER_HEAD`
3. 设置原版 `model_path`

```yml
info:
    namespace: playerheads
items:
  skull:
    enabled: true
    display_name: "SKULL"
    nbt: "{display:{Name:'{\"text\":\"Mossy Skull\"}'},SkullOwner:{Id:[I;-178232365,-1961341643,-1329297047,2014436438],Properties:{textures:[{Value:\"eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvYjk4NWQzOTY0NDhmM2NlMWQ0YWRhZGVjMjg2N2U5OGU4N2QxNTVhMjU2YmVmNmY0NjQxMDA1MzNiMjQ3YWMwYSJ9fX0=\"}]}}}"
    resource:
      material: PLAYER_HEAD
      generate: false
      model_path: "minecraft:item/player_head"
```

### 设置掉落物

我们必须创建一个新的掉落物配置，应该看起来像这样\
`OBSIDIAN` 是掉落此头部的方块\
↳ `namespace:blockname` 用于自定义 ItemsAdder 方块\
`head` 是自定义 ID，可以设置为任何您想要的值\
对 `item:` 我们应该放置准备好的头部的命名空间作为掉落物，所以是 `playerheads:skull`\
所有其他变量您可以在此处找到 https://itemsadder.devs.beer/plugin-usage/adding-content/loots.

```yml
info:
  namespace: my_loots
loots:
  blocks:
    obsidian:
      type: OBSIDIAN
      items:
        head:
          item: playerheads:skull
          min_amount: 1
          max_amount: 1
          chance: 100
```
