# 能不能创建自定义半砖、楼梯、三叉戟、盔甲等

### 台阶和楼梯

{% hint style="warning" %}
你无法创建实心的自定义台阶和楼梯。\
问题在于 Minecraft 不允许为自定义方块设置自定义碰撞箱。
{% endhint %}

（翻译者：其实你是否有注意过一个台阶叫做石化橡木台阶，只能指令获取，物品ID是petrified_oak_slab。你可以修改材质、语言名字再搭配自定义合成配方等等，不过就是这种东西得用镐子挖得快，硬度是石头，这只是我提供的思路，如果觉得太麻烦那还是不搞吧，可有可无 o^o）

### 三叉戟

{% hint style="warning" %}
你无法为投掷的三叉戟创建自定义模型，因为这是一个我无法修复的 Minecraft Bug：[https://bugs.mojang.com/browse/MC-155286](https://bugs.mojang.com/browse/MC-155286)
{% endhint %}

### 盔甲

{% hint style="warning" %}
Minecraft 1.16（及以下版本）不允许以任何方式为盔甲添加自定义纹理或自定义 3D 模型（可以，但只能通过 Optifine）。\
你可以改变盔甲的颜色，但不能改变其纹理。

### **1.17 自定义纹理盔甲**

要在 1.17 中创建自定义纹理盔甲，你可以按照[此处教程](../plugin-usage/adding-content/armors/custom-textured-armor.md)（无需 Optifine）进行操作。

### **1.16（及以下版本）自定义纹理盔甲**

ItemsAdder 可以自动为 1.16 及以下版本添加自定义盔甲，但前提是用户安装了 **Optifine**。\
只需在 `config.yml` 中启用该功能：

```yaml
generate-custom-armors-textures:
  optifine: true
```
{% endhint %}

### 鞘翅

{% hint style="warning" %}
Minecraft 不允许以任何方式为鞘翅添加自定义纹理或自定义 3D 模型。
{% endhint %}
