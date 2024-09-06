# API工具

## API工具

这些是一些静态工具，用于快速获取信息。

{% hint style="warning" %}
请注意，这些静态实用方法适用于快速使用，建议使用其他 API 类来进行操作。
{% endhint %}

```java
// 检查 ItemsAdder 是否已完成加载其所有物品以及是否可用
// 通常你应该使用 ItemsAdderFirstLoadEvent。
// 但有时你可能也需要通过编程方式检查这个。
public static boolean areItemsLoaded()

// 检查一个物品是否是使用 ItemsAdder 制作的自定义物品
public static boolean isCustomItem(ItemStack itemStack)
public static boolean isCustomItem(String customItemName)

// 返回世界中自定义方块的 ItemStack
public static ItemStack getCustomBlock(Block block)

// 检查世界中的实体是否是家具
public static boolean isFurniture(Entity entity)

// 检查 ItemStack 是否是特定的自定义物品
// （例如：检查一个镐是否是 'amethyst_pickaxe'）
public static boolean matchCustomItemName(ItemStack itemStack, String customItemName)
```

## 旧 API 方法

{% hint style="warning" %}
这是旧版 API，仍然可用且正常工作。
{% endhint %}

```java
// 根据配置中的名称获取 ItemsAdder 自定义物品
public static ItemStack getCustomItem(String nameInConfig)

// 使用 ItemStack 生成一个 ItemsAdder 制作的方块
// （通过 getCustomItem 获取）
public static void placeCustomBlock(Location location, ItemStack customBlock)
public static void placeCustomBlock(Location location, ItemStack customBlock, boolean lightweight)

// 获取自定义方块的掉落物品
public static List<ItemStack> getCustomBlockLoot(Block block, ItemStack tool, boolean includeSelfBlock)

// 检查世界中的方块是否是使用 ItemsAdder 制作的自定义方块
public static boolean isCustomBlock(Block block)

// 像正常玩家一样种植自定义种子
public static void placeCustomCrop(Location location, ItemStack seed)

// 检查方块是否是使用自定义种子种植的自定义作物
public static boolean isCustomCrop(Block block)

// 获取自定义作物的自定义种子名称
public static String getCustomSeedNameFromCrop(Block block)

// 获取配置中物品的名称（例如：'ruby_pickaxe'）
public static String getCustomItemName(ItemStack itemStack)

// 获取声明该物品的配置文件名称（例如：'items/swords'）
public static String getCustomItemFileName(ItemStack itemStack)

// 获取该物品剩余的使用次数（如果没有指定使用次数，则为 -999 = 无限）
public static int getCustomItemUsages(ItemStack itemStack)

// 设置自定义物品的耐久度（也适用于原版物品及具有默认原版耐久度的自定义物品）
public static ItemStack setCustomItemDurability(ItemStack item, int durability)

// 获取自定义耐久度
public static int getCustomItemDurability(ItemStack itemStack)

// 获取最大自定义耐久度
public static int getCustomItemMaxDurability(ItemStack itemStack)
```
