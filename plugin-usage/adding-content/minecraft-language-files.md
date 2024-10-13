# 📑 Minecraft语言文件

使用ItemsAdder，您可以轻松覆盖Minecraft的默认翻译文件。

### 使用示例：自定义ESC菜单

在此示例中，我将更改ESC菜单中的“返回游戏”文本。

```yaml
info:
  namespace: ia_various_configs
minecraft_lang_overwrite:
  esc_menu_texts:
    entries:
      "menu.returnToGame": "返回 &a生存 &f游戏模式"
    languages:
      - ALL
```

### `languages`

`languages` 属性用于列出您希望更改文本的所有语言。\
您应将其设置为仅包含您的玩家基础所使用的语言，但我决定将其设置为 `ALL`，以确保每个人都能看到自定义文本，无论他们选择的客户端语言是什么。

### `entries`

这是翻译文本的列表。 \
您可以在这里找到完整列表（请将 `1.19.3` 替换为您的版本）：

简体中文：[https://github.com/InventivetalentDev/minecraft-assets/blob/1.19.3/assets/minecraft/lang/zh_cn.json](https://github.com/InventivetalentDev/minecraft-assets/blob/1.19.3/assets/minecraft/lang/zh_cn.json)\
繁體中文（香港特別行政區）：[https://github.com/InventivetalentDev/minecraft-assets/blob/1.19.3/assets/minecraft/lang/zh_hk.json](https://github.com/InventivetalentDev/minecraft-assets/blob/1.19.3/assets/minecraft/lang/zh_hk.json)\
繁體中文（台灣）：[https://github.com/InventivetalentDev/minecraft-assets/blob/1.19.3/assets/minecraft/lang/zh_tw.json](https://github.com/InventivetalentDev/minecraft-assets/blob/1.19.3/assets/minecraft/lang/zh_tw.json)
