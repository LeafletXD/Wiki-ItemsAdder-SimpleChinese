# EpicBackpacks

## [点击下载EpicBackpacks插件](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-epic-backpacks.28981/)

{% hint style="warning" %}
你必须安装 [DefaultPack](../../first-install.md#default-pack-optional)！
{% endhint %}

{% hint style="success" %}
要创建使用 ItemsAdder 纹理的背包，你需要打开 EpicBackpacks 文件夹中的 `backpacks.yml` 并添加以下内容（每个背包都需要这样添加）：
{% endhint %}

```yaml
 cool_backpack:
    display_name: '&fCool Backpack'
    item:
      type: ITEMSADDER_ITEM
      name: "iageneric:plastic_bag"
    size: 3
    craft_recipe:
      pattern:
        - XXX
        - LCL
        - XLX
      ingredients:
        L: LEATHER
        C: CHEST
```
