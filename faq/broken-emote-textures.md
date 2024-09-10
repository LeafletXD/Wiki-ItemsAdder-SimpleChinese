---
描述: 动作存在纹理错误 (1.17+)
---

# 💃 动作纹理出现问题

## 着色器模组问题

允许使用自定义着色器的模组会破坏动作功能，因为它们会覆盖或替换 ItemsAdder 用于动作的原版着色器。

唯一的“修复”方法是禁用着色器或移除相应的着色器模组。

{% tabs %}
{% tab title="启用着色器（出现问题）" %}
![着色器问题](<../.gitbook/assets/image (51) (2) (1) (1).png>)
{% endtab %}

{% tab title="禁用着色器（无问题）" %}
![无着色器问题](<../.gitbook/assets/image (64).png>)
{% endtab %}
{% endtabs %}

已知引发问题的着色器模组：

### Optifine

相关问题：[https://github.com/sp614x/optifine/issues/6391](https://github.com/sp614x/optifine/issues/6391)

### IrisShaders

相关问题：[https://github.com/IrisShaders/Iris/issues/1042](https://github.com/IrisShaders/Iris/issues/1042)

## 修改玩家皮肤的模组

某些模组可能会更改默认的玩家模型/皮肤，因此可能会受到 ItemsAdder 着色器操作的影响，反之亦然。

已知引发问题的模组：

### 3DSkinLayers

该模组更改了外部皮肤层，使其以 3D 形式显示，从而更改了玩家模型。

可能的解决方法是禁用模组设置中的 `3D 头颅` 和 `3D 头颅物品`。\
目前，在动作动画中使用 3D 层没有解决方案。

有关更多信息，请参阅相关问题：[https://github.com/tr7zw/3d-Skin-Layers/issues/45](https://github.com/tr7zw/3d-Skin-Layers/issues/45)

### Customizable Player Models

该模组允许完全自定义玩家模型，包括替换部分或整个模型。\
因此，在 ItemsAdder 中动作无法正确显示，除非停止使用该模组或动作动画，目前没有其他修复方案。
