# 📓 Denizen API

{% hint style="warning" %}
需要 ItemsAdder 3.2.4 及以上版本
{% endhint %}

## 下载最新构建版本

{% embed url="https://ci.citizensnpcs.co/job/Denizen/" %}

## 功能

```yaml
# 检查物品是否为自定义物品
player.item_in_hand.is_ia_item
# 检查物品是否为自定义方块
player.item_in_hand.is_ia_block
# 获取物品的命名空间 ID
player.item_in_hand.ia_namespaced_id

# 放置自定义方块。
# 语法 set_custom_block [<location>|...] [<namespaced_id>]
set_custom_block <context.location> ruby_block 
# 检查方块是否为自定义方块
context.location.is_ia_block
# 获取方块的命名空间 ID
context.location.ia_namespaced_id
```

## 示例

```yaml
my_world_script:
    type: world
    events:
        after player left clicks block:
            - narrate " "
            - if <player.item_in_hand.is_ia_block>:
                - narrate "左击物品是一个自定义方块！ <&6><player.item_in_hand.ia_namespaced_id>"
            - else:
                - narrate "左击物品不是自定义方块！ <&7><player.item_in_hand.material>"
            - narrate " "
        after player right clicks block:
            - if <player.is_sneaking>:
                - set_custom_block <context.location> ruby_block 
            - else:
                - narrate " "
                - if <player.item_in_hand.is_ia_item>:
                    - narrate "右击物品是一个自定义物品！ <&6><player.item_in_hand.ia_namespaced_id>"
                - else:
                    - narrate "右击物品不是自定义物品！ <&7><player.item_in_hand.material>"

                - if <context.location.is_ia_block>:
                    - narrate "交互的方块是一个自定义方块！ <&6><context.location.ia_namespaced_id>"
                - else:
                    - narrate "交互的方块不是自定义方块！"
                - narrate " "
```
