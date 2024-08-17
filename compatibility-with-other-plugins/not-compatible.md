# ⚠ 不兼容

_**与XX插件兼容吗？**_

我不能确切回答这个问题，因为我无法知道世界上每个插件的编码方式，但以下是可能引起问题的插件列表：

* 所有使用 **自定义资源包** 的插件（如果您有基本的资源包合并知识，可以使它们兼容，请确保不替换 ItemsAdder 文件，您就完成了）
* [CraftEnhance](https://www.spigotmc.org/resources/custom-recipes-and-crafting-craftenhance.65058/)，此插件会混乱 ItemsAdder 的自定义配方逻辑，并造成重复物品的错误。因此，请不要使用它
* 自定义合成台行为和配方的插件
* [LootChest](https://www.spigotmc.org/resources/lootchest.61564/) 可能会导致一些 [问题](https://github.com/LoneDev6/ItemsAdder/issues/15#issuecomment-512990849)
* 目前**不兼容**那些使用不同面来创建自定义纹理的 **插件** 和世界生成器。未来我会添加兼容性。

(注：建议先查看作者是否有在插件帖子或是插件的维基百科里写该插件兼容什么、支持什么）
