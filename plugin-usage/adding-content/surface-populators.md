# 🍄 地表生成器

## 在世界表面生成装饰物

使用 ItemsAdder，您可以在世界各地生成装饰物，使您的服务器更专业和独特。

例如，您可以生成新的蘑菇、小植物、石头等装饰物。

![](../../.gitbook/assets/leaves.png)

![](../../.gitbook/assets/desert\_rose.png)

## 创建表面装饰生成器

### 创建配置文件

例如，让我们创建一朵玫瑰，它将在世界各地生成。

```yaml
info:
  namespace: myitems
surface_decorators:
  rose:
    block: rose
    bottom_blocks:
    - DIRT
    - GRASS_BLOCK
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
    chance: 10
    max_height: 255 
    min_height: 0
    amount: 1
```

如您所见，我设置了一些属性：

- `block` 是要作为装饰生成的 ItemsAdder 方块。
- `bottom_blocks` 属性用于决定装饰可以生成在哪些方块类型上。
- `biomes` 属性用于决定装饰可以生成在哪些有效生物群系中。
- `worlds` 属性决定装饰可以在哪些世界中生成。
- `chance` 是装饰在世界的每个区块中生成的概率。
- `max_height` 是装饰可以生成的最大世界高度。
- `min_height` 是装饰可以生成的最小世界高度。
- `amount` 是生成装饰组中的方块数量，例如，您可以设置为5，使一组5个装饰方块相连生成。

## 创建方块

现在，您只需按照教程创建方块。您可以根据需要使用 `REAL_NOTE`、`REAL_WIRE`、`REAL_TRANSPARENT` 和 `REAL` 方块。

{% content-ref url="block/create-a-block.md" %}
[create-a-block.md](block/create-a-block.md)
{% endcontent-ref %}

## 示例

您可以在此处下载完全可用的附加组件：

{% embed url="https://www.spigotmc.org/resources/deco-worlddeco-add-autogenerating-decorations-on-your-world-surface.95207" %}

![](../../.gitbook/assets/worlddeco\_ia.png)
