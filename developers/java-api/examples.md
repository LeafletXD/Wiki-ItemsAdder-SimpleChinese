# 用法

## 获取 API

{% embed url="https://github.com/LoneDev6/API-ItemsAdder" %}

## 自定义物品 - [文档](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomStack.java)

#### 通过 ID 或 `namespace:id` 获取任意类型的自定义物品（方块、物品、帽子、食物等）

```java
CustomStack stack = CustomStack.getInstance("your_item")
if(stack != null)
{
    ItemStack itemStack = stack.getItemStack();
}
else
{
    // 没有找到对应 id 的自定义物品
}
```

#### 检查自定义物品是否存在

```java
CustomStack.isInRegistry("your_item")
```

#### 通过 Bukkit `ItemStack` 获取 `CustomStack`

```java
CustomStack stack = CustomStack.byItemStack(myItemStack);

if(stack != null) // 是自定义物品！
{
    stack.setUsages(5) // 例如设置使用次数
    // ...
}
else // 不是自定义物品！
{
     // ...
}
```

## 自定义方块 - [文档](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomBlock.java)

#### 检查自定义方块是否存在

```java
CustomBlock.isInRegistry("your_item")
```

#### 检查世界中的方块是否为自定义方块

```java
CustomBlock customBlock = CustomBlock.byAlreadyPlaced(block);
if(customBlock != null)
{
    // 自定义方块，可以在这里执行自定义操作
}
else
{
    // 不是自定义方块
}
```

#### 放置自定义方块

```java
CustomBlock customBlock = CustomBlock.getInstance("ruby_ore");
if(customBlock != null) // 如果确定方块存在则不需要检查。
{
    customBlock.place(location);
}
else
{
    // 在 ItemsAdder 配置中找不到自定义方块！
}
```

## 自定义实体 - [文档](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomEntity.java)

#### 通过 ID 或 `namespace:id` 生成自定义生物

```java
CustomEntity customEntity = CustomEntity.spawn("your_item", location)
if(customEntity != null)
{
    // 自定义生物生成成功
    
    // 例如：在控制台打印命名空间 ID
    System.out.println(customEntity.getNamespacedID());
}
else
{
    // 在 ItemsAdder 配置中找不到自定义生物！
}
```

### 通过已生成的 Bukkit 实体获取自定义实体

```java
CustomEntity customEntity = CustomEntity.byAlreadySpawned(entity)
if(customEntity != null)
{
    // 是自定义实体
    
    // 例如：在控制台打印命名空间 ID
    System.out.println(customEntity.getNamespacedID());
}
else
{
    // 这个 Bukkit 实体不是自定义实体！
}
```

## 液体 API

请安装 [IALiquids](https://www.spigotmc.org/resources/84386) 插件以测试液体功能

```java
@EventHandler
void interact(PlayerInteractEvent e)
{
    if(e.getAction() == Action.LEFT_CLICK_BLOCK)
    {
        ItemsAdder.setLiquid("ialiquids:red_water", e.getClickedBlock().getLocation());
    }
    else if(e.getAction() == Action.RIGHT_CLICK_BLOCK)
    {
        System.out.println(ItemsAdder.getLiquidName(e.getClickedBlock().getRelative(e.getBlockFace()).getLocation()));
    }
}
```

## 使用 API 修改 HUD 值

### 设置 Frames HUD 中的浮点值

```java
PlayerHudsHolderWrapper playerHudsHolderWrapper = new PlayerHudsHolderWrapper(playerObject);
PlayerQuantityHudWrapper hud = new PlayerQuantityHudWrapper(playerHudsHolderWrapper, "namespace_name:hud_name");
hud.setFloatValue(1f);
```

### 设置 HUD 可见

```java
PlayerHudsHolderWrapper playerHudsHolderWrapper = new PlayerHudsHolderWrapper(playerObject);
PlayerQuantityHudWrapper hud = new PlayerQuantityHudWrapper(playerHudsHolderWrapper, "namespace_name:hud_name");
hud.setVisible(true);
```

## 旧版功能：

### 自定义生物 <mark style="color:orange;">(旧版)</mark> - [文档](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/CustomMob.java)

#### 通过 ID 或 `namespace:id` 生成自定义生物

```java
CustomMob customMob = CustomMob.spawn("your_item", location)
if(customMob != null)
{
    // 自定义生物生成成功
    
    // 例如：在控制台打印显示名称
    System.out.println(customMob.getName());
}
else
{
    // 找不到对应 id 的自定义生物
}
```

#### 获取已经生成的自定义生物

```java
CustomMob customMob = CustomMob.byAlreadySpawned(entity)
if(customMob != null)
{
    // 是自定义生物
    
    // 例如：在控制台打印显示名称
    System.out.println(customMob.getName());
}
else
{
    // 这个生物不是自定义生物
}
```
