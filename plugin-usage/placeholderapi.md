# 📎 特殊占位符

## PlaceholderAPI

### FontImage（字符图像、表情符号等）

代码是：`%img_NAME%`，其中 `NAME` 替换为字体图像名称。\
例如：`%img_smile%`

### 偏移量

你可以向前或向后移动文本/字体图像。\
例如：

* 向后移动 16 像素，写作 `%img_offset_-16%`
* 向前移动 16 像素，写作 `%img_offset_16%`

### ItemsAdder 玩家统计数据（HUD 值）

这些是 ItemsAdder 使用的统计数据，而非原版统计数据。

代码是：`%iaplayerstat_NAME%`，其中 `NAME` 替换为玩家统计数据名称。\
例如：`%iaplayerstat_mana%` 或 ` %iaplayerstat_thirst%`

你可以使用此命令进行测试：\
`/papi parse me %iaplayerstat_thirst%`\
`/papi parse me %iaplayerstat_mana%`

{% hint style="info" %}
#### 了解更多关于玩家统计数据的信息
{% endhint %}

## ItemsAdder 内置占位符（无 PlaceholderAPI）

### FontImage（字符图像、表情符号等）

代码是：`:img_NAME:`，其中 `NAME` 替换为字体图像名称。\
例如：`:img_smile:`

### 偏移量

你可以向前或向后移动文本或字体图像。\
例如：

* 向后移动 16 像素，写作 `:img_offset_-16:`
* 向前移动 16 像素，写作 `:img_offset_16:`

### ItemsAdder 玩家统计数据（HUD 值）

这些是 ItemsAdder 使用的统计数据，而非原版统计数据。

代码是：`:iaplayerstat_NAME:`，其中 `NAME` 替换为玩家统计数据名称。\
例如：`:iaplayerstat_mana:` 或 `:iaplayerstat_thirst:`
