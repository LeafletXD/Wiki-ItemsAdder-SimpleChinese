# 📃 配方菜单

## 菜单设置和 "全部" 类别

`ia_gui.yml` 包含关于 `/ia` 命令 GUI 的设置。\
它还包含 **"all"** 类别，显示所有 ItemsAdder 物品。

{% hint style="info" %}
默认的 ItemsAdder 包类别位于每个 `namespace` 文件夹中的 `categories.yml` 文件中。\
例如：`contents/iasurvival/configs/categories.yml`
{% endhint %}

## 创建自定义类别

如果您想创建自己的类别，需要在您的 [namespace](broken-reference) 中创建并将其添加到自己的 `.yml` 文件中。\
<mark style="color:red;">不要将您的类别添加到</mark> <mark style="color:red;"></mark><mark style="color:red;">`ia_gui.yml`</mark> <mark style="color:red;"></mark><mark style="color:red;">文件中！</mark>\
以下是一个示例：

```yaml
info:
  namespace: my_items
categories:
  swords:
    enabled: true
    icon: "my_items:custom_item"
    name: 'Swords'
    permission: "ia.menu.seecategory.swords"
    # 这是可选的。如果未设置，插件将使用 ia_gui.yml 中的配置。
    font_image:
      name: "mcguis:blank_menu"
      x_position_pixels: -16
    # 这是可选的。如果未设置，插件将使用 ia_gui.yml 中的配置。
    title_position_pixels: 0
    items:
      - "my_items:custom_item"
      - "my_items:custom_item_2"
      - "my_items:custom_item_3"
```

记得为每个类别授予用户权限，用户才可以看到这些类别。\
此示例类别的权限是：`ia.menu.seecategory.swords`

{% hint style="info" %}
**`font_image` 和 `title_position_pixels` 是可选的。**\
如果未设置，插件将使用 `ia_gui.yml` 中的配置。

如果您希望为每个类别设置不同的背景，这个选项非常有用。
{% endhint %}

{% hint style="success" %}
具有相同名称但不同命名空间的 **类别将会合并**，如果您有两个 "swords" 类别，这将非常 **有用**。\
这使您可以打开 **`/ia`** 菜单，并在同一个类别中看到所有剑，而不是有两个剑的类别。
{% endhint %}

## 批量添加物品到类别

{% hint style="warning" %}
需要 ItemsAdder 3.5.1 或更高版本。
{% endhint %}

### 通配符

匹配任何具有 `example` 命名空间的物品。

```yml
categories:
  test:
    enabled: true
    skip_if_already: false
    icon: example:my_item
    name: TEST
    permission: ia.menu.seecategory.test
    items:
      - example:*
```

匹配任何具有 `some_item` 物品的命名空间。

```yml
categories:
  test:
    enabled: true
    skip_if_already: false
    icon: example:my_item
    name: TEST
    permission: ia.menu
```

### 正则表达式（进阶）

匹配 `iasurvival` 命名空间中的任何盔甲物品。

{% hint style="info" %}
使用 [此网站](https://regex101.com/) 测试您的正则表达式。
{% endhint %}

```yml
  armors:
    enabled: true
    skip_if_already: false
    icon: iasurvival:ruby_helmet
    name: display-category-armors
    permission: ia.menu.seecategory.armors
    items:
      - iasurvival\:(.*)_helmet
      - iasurvival\:(.*)_chestplate
      - iasurvival\:(.*)_leggings
      - iasurvival\:(.*)_boots
```
