---
描述: 使用自定义着色器模组时（1.17+），盔甲纹理看起来是损坏了
---

# 使用光影时材质出现了问题

{% hint style="warning" %}
**ItemsAdder 3.0.3 中有此问题的临时修复方法**

**注意：** 此修复需要在游戏中安装 **Optifine** 或等效的 **CIT 模组**（如 **CIT Resewn**）。

如果你看到损坏的纹理，请确保使用的是 ItemsAdder 3.0.3 或更新的版本。\
同时，确保使用 `/iazip` 重新生成了资源包（如有需要，请阅读 [托管教程](../../plugin-usage/resourcepack-hosting/)）。
{% endhint %}

{% hint style="danger" %}
**Optifine** 1.19.3 和 1.19.4 当前存在问题，我对此无能为力。\
这些版本不支持我的修复方法。\
我们需要等待 **Optifine** 开发者来解决这个问题。

这不是我的错。
{% endhint %}

![](../../.gitbook/assets/shader_armor_bug.png)

![](../../.gitbook/assets/144463413-21137314-66a3-41de-a834-9c6063e65e83.png)

{% embed url="https://youtu.be/cb8OAuQE6V0" %}

## 此问题的原因是什么？

### Optifine 问题

Optifine 存在一个限制，当你安装了任何自定义的 Optifine 着色器时，无法正确显示自定义盔甲。

你需要暂时禁用 **Optifine** 着色器，或者暂时接受这个问题。

我已联系 Optifine 开发者：[https://github.com/sp614x/optifine/issues/6391](https://github.com/sp614x/optifine/issues/6391)

### Iris Shaders 问题

Iris 存在一个限制，当你安装了任何自定义的 Iris 着色器时，无法正确显示自定义盔甲。

我已联系 Iris 开发者：[https://github.com/IrisShaders/Iris/issues/1042](https://github.com/IrisShaders/Iris/issues/1042)
