# ExcellentEnchants

[点击下载](https://www.spigotmc.org/resources/goldenenchants-%E2%80%A2-more-vanilla-like-enchantments-1-14-1-16.61693/)

（以前称为 **GoldenEnchants**）

## 如何使用附魔

这是一个 ItemsAdder 自定义物品附魔的示例配置。

{% hint style="warning" %}
警告：附魔不会显示在物品的描述中，这是其他插件的一个“bug”。

<mark style="color:green;">效果仍然会生效！</mark>

因此，你需要自己编写描述。
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
    - tunnel:1
```

在这个例子中，我为 `ruby_pickaxe` 设置了 `tunnel` 附魔，等级为 1。
