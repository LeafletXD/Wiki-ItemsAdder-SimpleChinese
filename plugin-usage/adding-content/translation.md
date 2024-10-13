# 📚 翻译

## 支持翻译内容：

* 物品名称
* 物品描述（lore）
* `/ia` 菜单分类名称

## 翻译物品

### 翻译 ItemsAdder 默认物品

如果你想翻译 IA 默认物品，你只需复制我的字典并创建你自己的。

* 打开文件夹 `plugins/ItemsAdder/contents/`，并查找 `dictionaries` 文件夹（在每个目录中，例如 `iasurvival/configs/`）
* 复制并重命名文件 `en.yml`
* 将 `dictionary-lang` 从 `en` 改为你的语言标识符（例如 `fr`）
* 翻译你想要的内容
* 打开 config.yml 并将 `dictionaries-lang` 设置为你的语言标识符（例如 `fr`）
* 重载插件或重启服务器

### 为你新增的物品创建自己的翻译

要为你的自定义物品创建翻译，你只需在 `ItemsAdder/contents/` 文件夹内创建新文件夹，并在该文件夹内为每种语言创建新文件（每种语言一个文件），例如 `ItemsAdder/contents/myitems/configs/dictionaries/`。

示例如下：

```yaml
info:
  namespace: special_items_lang
  dictionary-lang: "fr"
dictionary:
  display-name-my_sword: épée de saleté
  display-name-my_item: j'aime la baguette
```

而我的物品文件看起来如下：

```yaml
info:
  namespace: special_items
items:
  my_sword:
    display_name: display-name-my_sword
    permission: my_sword
    resource:
      material: DIAMOND_SWORD
      generate: true
      textures:
      - item/my_sword.png
    durability:
      max_custom_durability: 1324
```

{% hint style="info" %}
如你所见，我将 `display_name` 设置为 `display-name-my_sword`，这会告诉 IA 使用字典中的文本替换，从而使剑的名称为 `épée de saleté`。
{% endhint %}

{% hint style="warning" %}
你可以**跳过**翻译部分，直接这样做，**但是**这样**不会**让你在将来需要时轻松**翻译**物品。

```yaml
info:
  namespace: special_items
items:
  my_sword:
    display_name: "épée de saleté"
    permission: my_sword
    resource:
      material: DIAMOND_SWORD
      generate: true
      textures:
      - item/my_sword.png
    durability:
      max_custom_durability: 1324
```
{% endhint %}

## 翻译命令和消息

你只需打开 `lang` 文件夹，复制 `en.yml`，然后翻译它，并在 `config.yml` 中将 `lang` 设置更改为你的文件名。
