# 我已删除了方块，后台提示该ID被占用

如果你确定可以使用以下命令清理插件缓存：`/iacleancache`  
此命令将删除所有缓存的 ID，以便你可以重新使用已移除方块的旧 ID。

{% hint style="info" %}
#### 为什么 ItemsAdder 需要方块 ID 缓存？

缓存存在的原因是，如果你错误地移除了一个方块，然后又想将其添加回来，它将使用相同的旧 ID，而不是每次都分配一个新的 ID。
{% endhint %}
