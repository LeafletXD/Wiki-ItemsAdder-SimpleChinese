# 💎 世界生成器

### 示例：两个生成器
{% hint style="warning" %}
<mark style="color:red;">不要忘记命名空间！</mark>\
每个配置文件都需要定义命名空间！
{% endhint %}

```yaml
info:
  namespace: my_world_populator
worlds_populators:
  custom_block:
    block: myitems:custom_block
    worlds:
    - world
    replaceable_blocks:
    - STONE
    - DIRT
    - ANDESITE
    - GRANITE
    - COBBLESTONE
    - GRAVEL
    biomes:
    - PLAINS
    chunk_chance: 70.0
    max_height: 45
    min_height: 25
    vein_blocks: 6
    chunk_veins: 1
  custom_block_2:
    block: myitems:custom_block_2
    worlds:
    - world
    replaceable_blocks:
    - DIRT
    chunk_chance: 100.0
    max_height: 64
    min_height: 40
    vein_blocks: 3
    chunk_veins: 1
```

这段代码允许你告诉 ItemsAdder 在名为 `world` 的世界中生成 `myitems:custom_block` 方块，并仅替换 `STONE`、`DIRT`、`ANDESITE`、`GRANITE`、`COBBLESTONE` 和 `GRAVEL` 类型的方块，且仅在 `PLAINS` 生物群系中生成。\
它将在每个区块中生成一条由 3 个方块组成的矿脉。

### `vein_blocks`、`chunk_veins`、`chunk_chance`

{% hint style="warning" %}
建议从我在 **ItemsAdder** 文件夹中创建的 `blocks.yml` 文件中读取数值。\
不要设置过高的数值，否则服务器可能会卡顿。\
请参考我的数值作为示例。
{% endhint %}

**`chunk_veins`**：每个区块中生成的矿脉数量\
**`vein_blocks`**：每条矿脉中的方块数量（或矿脉大小）\
**`chunk_chance`**：在区块中生成的几率。对于常见矿石，建议设置为 100，对于稀有矿石则可以调低。

{% hint style="warning" %}
<mark style="color:red;">**旧版 ItemsAdder**</mark> 3.1.6 之前的版本使用这些属性：\
`chunk_veins` -> `iterations`

`vein_blocks` -> `amount`

`chunk_chance` -> `chance`
{% endhint %}

### 生物群系

你可以删除此选项，插件会在所有生物群系中生成矿石。

```yaml
  custom_block:
    block: myitems:custom_block
    worlds:
    - world
    replaceable_blocks:
    - STONE
    - DIRT
    - ANDESITE
    - GRANITE
    - COBBLESTONE
    - GRAVEL
    chunk_chance: 70.0
    max_height: 45
    min_height: 25
    vein_blocks: 6
    chunk_veins: 1
```

### 可替换方块

你可以删除此选项，插件会在不检查是否可替换的情况下生成矿石并替换所有方块。

```yaml
  custom_block:
    block: myitems:custom_block
    worlds:
    - world
    chunk_chance: 70.0
    max_height: 45
    min_height: 25
    vein_blocks: 6
    chunk_veins: 1
```
