# 🪨 洞穴生成器

## 在洞穴中生成装饰物

{% hint style="warning" %}
此功能需要 **ItemsAdder** 3.1.6 及以上版本
{% endhint %}

使用 ItemsAdder，你可以在世界的洞穴中生成装饰物，使你的服务器更加专业和独特。

例如，你可以生成新的蘑菇、小植物、石头和其他装饰物。

![](<../../.gitbook/assets/image (81).png>)

## 创建洞穴装饰生成器

### 创建配置文件

例如，让我们创建一组小石头，它们会在世界各地生成。

```yaml
info:
  namespace: myitems
cave_decorators:
  small_rocks:
    block: small_rocks
    bottom_blocks:
    - DIRT
    - GRASS_BLOCK
    - STONE
    - COBBLESTONE
    - MOSSY_COBBLESTONE
    biomes:
    - PLAINS
    - SUNFLOWER_PLAINS
    - RIVER
    - MOUNTAINS
    - MOUNTAIN_EDGE
    - BIRCH_FOREST
    - BIRCH_FOREST_HILLS
    - TALL_BIRCH_FOREST
    - TALL_BIRCH_HILLS
    worlds:
      - world
    chance: 100
    max_height: 255 
    min_height: 0
    amount: 4
    position: SURFACE
```

如你所见，我设置了一些属性：

- `block` 是要作为装饰物生成的 ItemsAdder 方块。
- `bottom_blocks` 属性用于决定装饰物可以生成在哪些类型的方块上。
- `biomes` 属性用于选择装饰物可以生成的有效生物群系。
- `worlds` 属性决定装饰物可以生成的世界。
- `chance` 是装饰物在每个区块生成的几率。
- `max_height` 是装饰物可以生成的最高世界高度。
- `min_height` 是装饰物可以生成的最低世界高度。
- `amount` 是每组装饰物生成的数量，例如，你可以设置为 5，这样会生成 5 个相连的装饰物。
- `position` 属性用于指定方块必须在洞穴的 `SURFACE`（表面）还是 `CEILING`（天花板）上。

## 创建方块

现在，你只需按照教程创建方块。你可以使用 `REAL_NOTE`、`REAL_WIRE`、`REAL_TRANSPARENT` 和 `REAL` 方块，具体取决于你的需求。

{% content-ref url="block/create-a-block.md" %}
[创建一个自定义方块](block/create-a-block.md)
{% endcontent-ref %}
