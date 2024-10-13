# ⚡ 快速使用的小技巧

## 编辑资源包并上传到服务器花费了太多时间！

如果你方法不对，确实会花很多时间。请阅读以下内容：

{% hint style="info" %}
建议在你的电脑上创建一个 **测试服务器**，并使用以下插件：

* [ItemsAdder](https://www.spigotmc.org/resources/%E2%9C%85must-have%E2%9C%85-itemsadder%E2%9C%A8textures-3d-models-emojis-ores-blocks-wings-tails-hats-more.73355/)
* [LoneLib](https://www.spigotmc.org/resources/lonelibs.75974/)
* [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/)

使用以下 ItemsAdder 的资源包配置：

```yaml
resource-pack:
  hosting:
    no-host:
      enabled: false
    auto-external-host:
      enabled: false
    self-host:
      enabled: true # <----- 在此处设置为 true
      server-ip: '127.0.0.1' # <----- 在此处输入你的服务器IP地址，不要加端口！
      pack-port: 8163 # <----- 在此处输入一个空闲的/额外的/开放的端口！
    external-host:
      enabled: false
```

这样，你将拥有一个快速且易于使用的配置环境。\
你可以实时添加物品并编辑资源包。

当你编辑物品的材质或模型并更改其配置时，使用指令 `/iazip`。\
这样你就可以实时看到所做的更改。

在完成物品添加和配置后，你可以将所有内容上传到你的服务器，以同步这些更改。
{% endhint %}

{% hint style="warning" %}
建议不要直接在服务器上编辑 ItemsAdder 的材质和模型。\
玩家不喜欢插件重载时的卡顿、服务器重启，以及在游戏过程中重新下载资源包……\
最好是在本地测试服务器上进行编辑和测试。
{% endhint %}

{% hint style="warning" %}
不要忘记！这是适合你服务器的最佳设置，最快速且在上传资源包时不需要任何维护。
{% endhint %}

{% hint style="danger" %}
建议不要编辑我的自定义物品。\
将来我会对它们进行更新，而你将会在维护自定义内容和我的更新之间感到头疼。\
建议创建你自己的物品。
{% endhint %}
