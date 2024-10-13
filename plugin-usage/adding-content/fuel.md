# 🛢 燃料

## 创建物品

{% hint style="warning" %}
你必须使用在原版 Minecraft 中可以熔炼的材料，否则它将无法正常工作。\
例如：`STICK`、`COAL`、`CHARCOAL` 等。
{% endhint %}

例如，以下配置将使该物品可用于 **BLAST_FURNACE**，并在 **20 ticks** 内燃烧（**1 秒**）。

```yaml
  magic_fuel:
    display_name: "%#FE5A00%magic_fuel"
    permission: fuel.magic_fuel
    resource:
      material: COAL
      generate: false
      model_path: item/diamond
    behaviours:
      fuel: 
        burn_ticks: 20
        machines:
          - BLAST_FURNACE
```
