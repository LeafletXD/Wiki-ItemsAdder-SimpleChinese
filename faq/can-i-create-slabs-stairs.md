# 能不能创建自定义半砖、楼梯、三叉戟、盔甲等

### 台阶、楼梯

{% hint style="warning" %}
你无法创建自定义的实体台阶、楼梯和其他可放置的实体物品（除方块外）。原因是 Minecraft 存在一个 bug，导致这些物品显示为透明方块：[https://bugs.mojang.com/browse/MC-54254](https://bugs.mojang.com/browse/MC-54254)。当 Mojang 修复这个问题后（添加一个可以开启或关闭的特殊标签，现在默认开启 **“Opaque”**），你将能够创建自定义形状的方块。

另一个原因是我无法更改方块的碰撞箱，遗憾的是这是 Minecraft 的一个限制。
{% endhint %}

（翻译者：其实你是否有注意过一个台阶叫做石化橡木台阶，只能指令获取，物品ID是petrified_oak_slab。你可以修改材质、语言名字再搭配自定义合成配方等等，不过就是这种东西得用镐子挖得快，硬度是石头，这只是我提供的思路，如果觉得太麻烦那还是不搞吧，可有可无o^o）

### 三叉戟

{% hint style="warning" %}
你无法为投掷后的三叉戟创建自定义模型，因为这是一个 Minecraft 的 bug，我无法修复：[https://bugs.mojang.com/browse/MC-155286](https://bugs.mojang.com/browse/MC-155286)
{% endhint %}

### 盔甲

{% hint style="warning" %}
Minecraft 不允许以任何方式为盔甲添加自定义纹理或自定义 3D 模型。你可以更改盔甲颜色，但无法更改其纹理。
{% endhint %}

{% page-ref page="../plugin-usage/adding-content/creating-a-custom-item/armor.md" %}
