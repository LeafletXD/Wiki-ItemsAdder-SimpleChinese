# 🗂 内容文件夹

## 文件夹类型

### contents

这是一个包含子文件夹的主文件夹。\
每个子文件夹包含一个独立的包，其中包含配置、模型、纹理、声音等文件。

在 **contents** 文件夹中，每个子文件夹的名称即是它所包含资源的 [namespace](broken-reference)。

### configs

每个 `contents` 文件夹都包含一个名为 `configs` 的子文件夹。\
这个文件夹内有多个文件和子文件夹。\
其中包含 `.yml` 文件，这些文件定义物品的行为、设置、附魔、配方、掉落、物品属性等。

{% hint style="warning" %}
**Namespace** 也需要在 `.yml` 文件中设置，不要忘记在文件的顶部添加：

```yaml
info:
  namespace: example
```
{% endhint %}

### resourcepack

可以将此文件夹与 **configs** 文件夹视为类似的内容，但 **resourcepack** 文件夹包含所有 **物品** 的“图形”部分（以及声音、GUI 等等）。

{% hint style="danger" %}
#### **重要提示**

始终保持 **contents** 子文件夹的有序性！\
不要随意粘贴文件，不要创建太多子文件夹，避免遗留未使用的纹理/模型，否则查找错误时会非常困难。
{% endhint %}

## 什么是 `namespace`？

正如你可能已经注意到的，ItemsAdder 使用 **`namespaces`** 来标识它所管理的大多数事物。\
**`namespace`** 是元素的 **组**，在本例中是 **物品、方块、怪物等** 的组。\
通过命名空间，你可以轻松了解某个特定的 **物品**、**声音**、**方块** 等来自哪里。

### 示例

所有 **realcraft** 物品都在 **realcraft** 命名空间下，因此当你使用 `/iaget` 命令时，可以看到所有物品的 ID 都以 `realcraft:` 开头。

![](<../../.gitbook/assets/image (7).png>)

## 如何定义我自己的命名空间？

为了保持一切井然有序，你需要创建 **你自己的命名空间**。\
第一步是在: `plugins/ItemsAdder/contents/` 下创建一个子文件夹。

在这个例子中，命名空间将是 `my_items`，因此你需要创建一个名为 `contents/my_items/` 的文件夹。

![](../../.gitbook/assets/my\_items\_namespace.png)

打开 `my_items` 文件夹并创建一个新文件，你可以根据自己的喜好命名。\
例如: `contents/my_items/myswords.yml`

![](../../.gitbook/assets/my\_swords\_yml.png)

打开新建的 `.yml` 文件并粘贴以下内容：

```yaml
info:
  namespace: my_items
```

如你所见，我将 **namespace** 设置为 `my_items`，这与之前选择的命名空间相同，且与 **文件夹** 名称一致。\
记得根据你的 **namespace** 进行更改。

{% hint style="info" %}
你可以创建任意数量的 **命名空间**！\
这可以帮助你轻松组织物品包。
{% endhint %}

{% hint style="info" %}
你可以在同一个命名空间中创建任意数量的 `.yml` 文件！\
这可以帮助你更好地组织物品类型。\
例如，我将物品分为剑、方块、食物、饮料等。
{% endhint %}

{% hint style="warning" %}
**所有这些“嵌套”看起来可能很繁琐，** 但它最大限度地减少了错误的发生，并让你能轻松找到所需内容。
{% endhint %}

## 为什么使用不同的文件夹结构？

**ItemsAdder** 允许你选择如何组织各种物品包的文件夹结构。

这对管理员来说非常有用，因为它提供了自由，可以快速组织物品包，而无需担心无用的文件夹嵌套。\
最简单的文件夹结构是 [结构 5](configs-and-resourcepack.md#folders-structure-method-5)。

{% hint style="warning" %}
每个子包只能使用一种结构。\
**不要在同一个子包中混用不同的结构！**
{% endhint %}

### 文件夹结构方法 1

这是默认的、最完整的结构。

```
plugins
└── ItemsAdder
    └── contents
        └── my_items
            ├── configs
            │   ├── example.yml
            │   └── example_1.yml
            └── resourcepack
                └── assets
                    └── my_items
                        ├── models
                        │   └── items
                        │       └── example_item.json
                        └── textures
                            └── items
                                └── example_texture.png
```

### 文件夹结构方法 2

这种结构避免了创建 `assets` 文件夹，因为它是隐含的，额外的复杂性是多余的。

```
plugins
└── ItemsAdder
    └── contents
        └── my_items
            ├── configs
            │   ├── example.yml
            │   └── example_1.yml
            └── resourcepack
                └── my_items
                    ├── models
                    │   └── items
                    │       └── example_item.json
                    └── textures
                        └── items
                            └── example_texture.png
```

### 文件夹结构方法 3

这种结构避免了创建 `resource_pack` 文件夹，因为它是隐含的，额外的复杂性是多余的。

```
plugins
└── ItemsAdder
    └── contents
        └── my_items
            ├── configs
            │   ├── example.yml
            │   └── example_1.yml
            └── assets
                └── my_items
                    ├── models
                    │   └── items
                    │       └── example_item.json
                    └── textures
                        └── items
                            └── example_texture.png
```

### 文件夹结构方法 4

这种结构避免了创建 `assets` 文件夹，因为它是隐含的，额外的复杂性是多余的。

```
plugins
└── ItemsAdder
    └── contents
        └── my_items
            ├── configs
            │   ├── example.yml
            │   └── example_1.yml
            └── my_items
                ├── models
                │   └── items
                │       └── example_item.json
                └── textures
                    └── items
                        └── example_texture.png
```

### 文件夹结构方法 5

{% hint style="success" %}
这是最简单的方式，可以快速创建包含一些物品的简单包，而不必创建太多子文件夹。\
它避免了创建 `resourcepack`、`assets` 和 `NAMESPACE` 文件夹，使一切更加简洁。
{% endhint %}

如果你的子包不使用多个命名空间，或者你不打算指定它们，这种方法会很有用。

```
plugins
└── ItemsAdder
    └── contents
        └── my_items
            ├── configs
            │   ├── example.yml
            │   └── example_1.yml
            ├── models
            │   └── items
            │       └── example_item.json
            └── textures
                └── items
                    └── example_texture.png
```
