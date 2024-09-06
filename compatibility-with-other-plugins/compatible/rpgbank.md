# RPGBank

## [点击下载](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-rpgbank-store-your-items-exp-and-money-using-villagers-npcs-and-custom-gui.29139/)

{% hint style="warning" %}
您必须安装 [DefaultPack](../../first-install.md#default-pack-optional)！
{% endhint %}

您可以更改 GUI 图标，并使用 ItemsAdder 图标来实现这一点：

![](<../../.gitbook/assets/image (13) (1).png>)

{% tabs %}
{% tab title="config.yml" %}
```yaml
  icons:
    money-indicator: coin
    next-page: icon_right_blue
    previous-page: icon_left_blue
    page-indicator: BLACK_STAINED_GLASS_PANE
    deposit-exp: icon_ender_chest
    locked: icon_lock
    deposit-money: icon_arrow_chest
```
{% endtab %}

{% tab title="语言文件" %}
```yaml
account-title: :offset_-16::blank_menu::offset_-176:&0{player}
```
{% endtab %}
{% endtabs %}
