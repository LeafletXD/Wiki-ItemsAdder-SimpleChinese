# 🔢 自定义玩家数据

## 什么是玩家数据？

它们是由 ItemsAdder 添加的自定义属性，您可以使用特殊命令 `/iaplayerstat` 来添加和读取这些属性。

然后，您可以使用 **PlaceholderAPI** 将它们显示在任何地方或绑定到 HUD。\
我这样做是为了创建口渴和魔法值。请查看我的 [默认配置](https://github.com/search?q=repo%3AItemsAdder%2FDefaultPack+player_stat_name&type=code) 以获取示例。

### 示例：

`/iaplayerstat write LoneDev thirst 6`\
`/iaplayerstat read LoneDev thirst float`

## 保存玩家统计数据

### 自定义 NBT 文件

将其保存到由 ItemsAdder 处理的自定义 NBT 文件中，这样可以很容易地删除此文件。\
此文件保存在 `plugins\ItemsAdder\storage\players\stats\` 文件夹中。

```yaml
player_stats:
  save_type: CUSTOM_NBT
```

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

### player.dat 文件

将其保存到原版的 `player.dat` 文件中。\
如果您想同步服务器，并且已经同步了玩家数据文件，这种方法非常有用。

```yaml
player_stats:
  save_type: PLAYER_DAT
```

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>
