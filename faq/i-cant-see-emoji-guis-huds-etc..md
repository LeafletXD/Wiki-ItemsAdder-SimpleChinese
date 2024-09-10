# 👀 我看不到表情符号、GUI、HUD等

## ItemsAdder 3.4.1 及更高版本

* 打开 **ItemsAdder** 的 `config.yml`
* 启用此选项：

    ```yaml
    fix_force_unicode_font_images: true
    ```
* 运行 `/iazip` 以重新生成资源包
* 按照插件安装过程中选择的[资源包托管方法教程](../plugin-usage/resourcepack-hosting/)进行操作

## ItemsAdder 3.4.0 及更低版本

如果你将 **强制使用Unicode字体** 设置为 **开启**，因为你不喜欢 Minecraft 的默认字体，你将无法看到表情符号、自定义 GUI 和 HUD。

通常在 Minecraft 中，你会将 **强制使用Unicode字体：开启** 设置为获取“细字体”。

![](../.gitbook/assets/image\_\(5\).png)

使用 **ItemsAdder** 时，这种设置将导致表情符号、GUI 和 HUD 无法正常工作。这是 Minecraft 的一个限制。

{% hint style="warning" %}
你必须将 **强制使用Unicode字体：关闭**
{% endhint %}

![](../.gitbook/assets/image\_\(6\).png)

并在 `config.yml` 中设置以下内容：

```yaml
  thin-font:
    enabled: true
```

这样，你可以将 **强制使用Unicode字体** 设置为 **关闭**，但仍然启用细字体。

{% hint style="warning" %}
请记住，进行此更改后，你需要重新生成 `generated.zip` 文件。\
查看[资源包教程](../plugin-usage/resourcepack-hosting/)
{% endhint %}

### 最终效果

![](../.gitbook/assets/image\_\(7\).png)

{% hint style="success" %}
现在你可以看到“细字体”，并且 GUI、表情符号和 HUD 不会再出现错误的白色方块。
{% endhint %}
