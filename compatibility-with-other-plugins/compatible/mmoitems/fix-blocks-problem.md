# 修复方块问题

{% hint style="warning" %}
**MMOItems** 方块与 **ItemsAdder** 不兼容，反之亦然。
{% endhint %}

## 如何使用 MMOItems 方块？

你需要打开 **ItemsAdder** 的 `config.yml` 文件并禁用 **REAL** 方块（蘑菇）。

{% code title="config.yml" %}
```yaml
blocks:
  # ....
  custom:
    # ....
    mushroom: false
```
{% endcode %}

{% hint style="info" %}
应用此更改后，你将无法创建类型为 REAL 的 ItemsAdder 方块。

其他 ItemsAdder 自定义块类型仍然可以正常使用（例如 REAL\_NOTE）。
{% endhint %}
