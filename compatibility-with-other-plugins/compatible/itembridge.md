# ItemBridge

## [点击下载](https://www.spigotmc.org/resources/77080/)

{% hint style="warning" %}
您需要 **ItemsAdder** 3.1.0 及以上的版本 和 **ItemBridge** 3.1 及以上的版本。
{% endhint %}

## 如何使用 ItemBridge 获取 ItemsAdder 自定义物品

要通过 **Mimic** 获取自定义物品，请使用以下命令：

`/ib get <mark style="color:blue;">ia:<item namespaced id></mark>`

`/ib give <player> <mark style="color:blue;">ia:<item namespaced id></mark>`

`/ib drop <world> <x> <y> <z> <mark style="color:blue;">ia:<item namespaced id></mark> [amount]`

### 示例

`/ib give LoneDev ia:itemsadder:ruby_sword`

{% hint style="warning" %}
重要的是在 ItemsAdder 自定义物品名称前加上 `ia:`，否则 **ItemBridge** 将无法识别它。

在这个例子中，`itemsadder:ruby_sword` 必须被指定为 `ia:itemsadder:ruby_sword`。
{% endhint %}
