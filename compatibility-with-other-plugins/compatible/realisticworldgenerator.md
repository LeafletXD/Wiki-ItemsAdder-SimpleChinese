# RealisticWorldGenerator

## [点击下载](https://www.spigotmc.org/resources/realisticworldgenerator-1-8-8-1-16-x.15905/)

## 兼容性

* 生物群系
* 矿物
* 结构 (RWG 结构)

{% hint style="warning" %}
此功能仅适用于 ItemsAdder 2.5.2+ 和 RealisticWorldGenerator 4.30+ 版本
{% endhint %}

## 注意事项

{% hint style="danger" %}
不要将自定义块用作基础矿石方块。这会导致严重的延迟。\
请继续使用原版方块来作为基础矿石方块。
{% endhint %}

{% code title="ores.yml" %}
```yaml
ores:
  veins:
    biome_layers:
      paste: false
    type: 1
    enabled: true
  base:
    block: ia:itemsadder:ruby_block # <---- 不要这样做！！！
```
{% endcode %}

{% hint style="success" %}
仅在以下情况下使用自定义方块：

* 表面
* 矿石
* 结构（结构图）
{% endhint %}

## 如何使用自定义块

例如，让我们创建一个具有 `ruby_block` 作为顶层的生物群系。

打开 **RealisticWorldGenerator** 世界配置文件夹中的 `biomes.yml` 文件。

选择一个生物群系（例如 `plains`），并将以下内容添加为第一层。

{% code title="biomes.yml" %}
```yaml
plains:
  layer:
    '1':
    - ia:itemsadder:ruby_ore;120
    '2':
    - minecraft:coarse_dirt;2
    - minecraft:podzol[snowy=false];5
    - minecraft:grass_block[snowy=false];100
```
{% endcode %}

在这个例子中，我还修改了这个世界的 `settings.yml` 文件，以确保只生成一个生物群系，便于找到我的自定义方块。

{% code title="settings.yml" %}
```yaml
one_biome:
  biome: PLAINS
  oceans: false
  enabled: true
```
{% endcode %}

### 最终效果

这是一个自定义表面的世界

![](<../../.gitbook/assets/image (41) (1).png>)
