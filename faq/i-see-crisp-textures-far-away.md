# 👁 我在远处看到了清晰的纹理！

{% hint style="warning" %}
如果你看到远处的纹理点状而且不平滑，这是资源包制作者的常见错误。\
Minecraft 有一个 bug，会在你设置的纹理尺寸不是 2 的幂时禁用 mipmap！
{% endhint %}

![左侧：无 mipmap。右侧：有 mipmap](<../.gitbook/assets/image (19).png>)

## **如何修复？**

很简单！只需按照以下步骤操作：

* 阅读本教程以了解 [如何阅读游戏日志](identify-why-textures-are-not-shown.md)（不是服务器日志）。
* 搜索文本 `limits mip level`
* 确定有问题的纹理，例如 `Texture mcicons:item/icon_toggle_off with size 30x30 limits mip level from 3 to 1`
* 修复纹理。\
  要修复它，你需要将其调整为以下尺寸之一：16x16、32x32、64x64、128x128、256x256 等。\
  你可以选择其中之一。
