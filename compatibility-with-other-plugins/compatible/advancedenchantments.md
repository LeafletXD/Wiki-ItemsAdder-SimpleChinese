# AdvancedEnchantments

## [点击下载](https://www.spigotmc.org/resources/43058/)

## 如何使用附魔

以下是为 ItemsAdder 自定义物品附魔设置的示例配置。

{% hint style="warning" %}
此功能需要 ItemsAdder 版本 2.5.2 或更高版本。
{% endhint %}

```yaml
  ruby_pickaxe:
    display_name: display-name-ruby_pickaxe
    permission: ruby_pickaxe
    resource:
      material: DIAMOND_PICKAXE
      generate: true
      textures:
      - item/ruby_pickaxe.png
    enchants:
    - ambit:7
```
