---
描述: 如何保护您的资源包不被盗用
---

# 🚨 保护资源包不被解压

{% hint style="warning" %}
## 免责声明

没有 100% 有效的方法可以保护资源包，因为游戏必须能够正确解压它以显示纹理。

此功能是为了防止孩子和恶作剧者盗取您的纹理。\
一些有经验的用户可能能够找到绕过这些保护措施的方法，只能防范无脑的暴力破解（压缩包直接解压）

ItemsAdder 已经尽力阻止这种情况，但请记住，世上没有完美的绝对防护......

其他插件也有相同的限制。这不是 ItemsAdder 的限制。
{% endhint %}

{% hint style="info" %}
使用 ItemsAdder，您可以保护您的资源包不被解压和盗用。\
您只需要在 config.yml 中设置此选项，并重新使用 /iazip。\
如果您使用的是 Dropbox，请不要忘记重新上传包并更新 config.yml。

{% code title="config.yml" %}
```yaml
  zip:
    protect-file-from-unzip:
      protection_1: true
      protection_2: true
```
{% endcode %}
{% endhint %}

## protection\_1

`protection_1` 属性允许您使用基本方法保护资源包。

## protection\_2

`protection_2` 属性允许您使用另一层保护来阻止一些其他解压包的方法。

## 展示

这是一个有趣的展示，展示了用户尝试盗取您的数据时会看到的内容。实际上，用户会看到一组损坏的文件和文件夹。

{% embed url="https://youtu.be/MhtEhoOuWV8" %}
