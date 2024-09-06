# AdvancedEnchantments

## [点击下载](https://www.spigotmc.org/resources/43058/)

## 如何使用附魔

{% hint style="info" %}
需要 4.0.2-beta-9 或更高版本。
{% endhint %}

这是一个 ItemsAdder 自定义物品附魔的示例配置。

```yaml
info:
  namespace: test
items:
  advanced_enchants_test:
    display_name: advanced_enchants_test
    resource:
      material: DIAMOND_SWORD
      generate: false
      model_path: minecraft:item/emerald
    enchants:
      - Beastslayer
      - Epicness
      - Immolation
```

{% hint style="warning" %}
## 警告

为了在 **ItemsAdder** 物品上使用自定义 **AdvancedEnchantments** 附魔，您需要在 **ItemsAdder** 的 config.yml 中启用此功能。

```yaml
advanced_enchantments:
  enable_custom_enchants_in_items_configs: true
```

但请注意，这有一个缺点。\
由于它们如何与我的插件挂钩，您将无法在 **AdvancedEnchantments** 的 [盔甲套装 | Armor Set](https://ae.advancedplugins.net/configuration/armor-sets) 功能中使用自定义盔甲材质。\
对此我无能为力。
{% endhint %}
