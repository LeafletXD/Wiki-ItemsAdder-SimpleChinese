# 简单示例

## 示例

### 命令：给予自定义物品

```yaml
command /iaskriptgetitem <text> [<number=1>]:
  trigger:
    set {%player%.item} to null
    set {%player%.item} to customitem arg 1
    if {%player%.item} is null:
      message "自定义物品 %arg 1% 未找到"
    else:
      give player arg 2 of {%player%.item}
      message "获得了自定义物品 %arg 1%"
```

### 命令：检查是否持有自定义物品

```yaml
command /iaskriptiscustomitem:
  trigger:
    if player's tool is a customitem:
      message "这是一个自定义物品"
    else:
      message "这不是一个自定义物品"
```

### FontImage（表情符号、GUI 等）

```yaml
command /emojitest:
  trigger:
    set {iconConfirm} to fontimage "twitteremojis:confirm"
    message "Good：%{iconConfirm}%"
```
