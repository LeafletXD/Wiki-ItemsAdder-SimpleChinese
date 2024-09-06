# Holographic Displays

## 如何在悬浮字中使用表情符号

* 下载 [Holographic Displays](https://dev.bukkit.org/projects/holographic-displays)
* 下载 [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)
* 下载 [HolographicExtension 插件](https://www.spigotmc.org/resources/holographicextension.18461/)

现在，您可以在悬浮字文本以及所有支持 **PlaceholderAPI** 的插件中使用 [字符图像](../../plugin-usage/adding-content/font-images/) (**表情符号**)。\
代码格式为 `%img_NAME%`，其中 NAME 是字体图像的名称。\
例如：`%img_smile%`

要创建一个悬浮字，您可以使用以下命令：

`/holo create test_itemsadder Hello! %img_smile%`

![](<../../.gitbook/assets/image (20).png>)

## 如何添加悬浮自定义物品？

* 运行 `/iacustommodeldata <item>`（例如 `/iacustommodeldata ruby`）
* 复制 `CustomModelData`，例如 `10000`
* 创建一个新的悬浮字，例如：`/hd create holo_icon Hello!`
* 通过指定 **vanilla type** 和 **CustomModelData** 将悬浮物品添加到悬浮字中。例如： `/hd addline holo_icon ICON: IRON_INGOT {CustomModelData: 10000}`

![](<../../.gitbook/assets/image_(124).png>)
