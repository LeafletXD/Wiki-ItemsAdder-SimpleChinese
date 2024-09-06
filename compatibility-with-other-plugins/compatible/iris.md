# Iris

## [点击下载](https://www.spigotmc.org/resources/iris-world-gen-custom-biome-colors.84586/)

## 启用兼容性

### 步骤 1

安装 [ItemsAdderBlocksInjector](https://www.spigotmc.org/resources/itemsadderblocksinjector.102078/)，并 <mark style="color:red;">安装后不要将其删除！</mark>

### 步骤 2

创建您的 Iris 世界（按照他们的指南进行），并像使用原版方块一样使用您的 ItemsAdder 自定义方块 ID。

例如，打开 `overworld` 包中的这个文件：`plugins\Iris\packs\overworld\biomes\mountain\mountain.json`

然后编辑图层设置以使用自定义块，例如自定义 **锡石矿石**：

```json
"layers": [
    {
        "minHeight": 1,
        "maxPerChunk": 21,
        "maxHeight": 80,
        "minPerChunk": 7,
        "minSize": 3,
        "maxSize": 7,
        "palette": [{ "block": "iasurvival:cassiterite_ore" }],
        "varience": 7
    },
```

这将生成类似于以下的效果：

![](<../../.gitbook/assets/image (49).png>)

![](<../../.gitbook/assets/image (96).png>)

## 兼容性问题

* FastAsyncWorldEdit 将无法工作，这点我无能为力。
* WorldEdit 的 `//undo` 和 `//copy` 将无法与 `Iris` 放置的自定义块一起使用，这些块会被还原为 `NOTE_BLOCK`（或 `mushroom`、`TRIPWIRE`、`CHORUS_PLANT`）。
