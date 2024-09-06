# HUDs、GUIs、图像及更多

要了解如何使用 HUDs 和 GUIs API（字体图像），可以查看我的示例。

## GUIs

{% embed url="https://github.com/LoneDev6/API-ItemsAdder-Example-GUI" %}

## HUDs

{% embed url="https://github.com/LoneDev6/RPGhuds" %}

{% embed url="https://github.com/LoneDev6/API-ItemsAdder-Example-ServerMonitor" %}

### 访问魔法值条的示例

```java
PlayerHudsHolderWrapper huds = new PlayerHudsHolderWrapper(player);
PlayerQuantityHudWrapper manaHud = 
                new PlayerQuantityHudWrapper(huds, "magiccraft:mana_bar");
if(manaHud.exists())
  manaHud.setFloatValue(2.0f);
else
  System.out.println("错误：未找到魔法值条，可能已被禁用。");
```

{% hint style="warning" %}
### 注意

确保你没有权限 `ia.user.hud.bypass.api.*`，否则 `setFloatValue` 方法将无效。
{% endhint %}

## 常见问题解答

{% content-ref url="../../plugin-usage/adding-content/font-images/common-errors.md" %}
[common-errors.md](../../plugin-usage/adding-content/font-images/common-errors.md)
{% endcontent-ref %}

## 获取表情符号或 GUI 字符

```java
new FontImageWrapper("twitteremojis:confirm").getString()
```
