# 📤 用DropBox托管

（翻译者：我**强烈不建议**使用该方法作为第三方托管，因为国内可能会出现墙或是下载过慢，建议使用**自托管**或是寻找其他稳定的文件托管平台，我用过Github和Gitee）

## 文本教程

* 打开 [DropBox](https://dropbox.com/)，注册/登录
* 使用命令 `/iazip` (**这很重要**，因为 `/iazip` 会重新加载配置并更新 **generated.zip** 文件)
* 打开文件夹：`plugins/ItemsAdder/output/`
* **拖放** 文件 **generated.zip** 到 **DropBox** 上
* 点击 **分享**

![](../../.gitbook/assets/image\_\(20\).png)

* 点击 **创建**

![](../../.gitbook/assets/image\_\(21\).png)

* 点击 **复制链接**
* 例如，如果您的链接是 [https://www.dropbox.com/blablabla?dl=0](https://www.dropbox.com/blablabla?dl=0)
* 打开 **ItemsAdder** 的 `config.yml`
* 设置如下（**我使用了示例 URL，请使用您自己的 URL**）

```yaml
resource-pack:
  apply-on-join: true
  kick-player-on-decline: false
  delay-ticks: 1
  self-host:
    enabled: false
  external-host:
    enabled: true
    url: 'https://www.dropbox.com/blablabla?dl=0'
```

* **这非常重要**：**使用命令** `/iareload` 来 **重新加载** **插件**，**在您更改** `config.yml` **后**（在这种情况下，重新加载资源包下载链接）
* **使用命令** `/iatexture` 在游戏中刷新您当前的游戏纹理，或使用 `/iatexture all` 为所有玩家刷新纹理

{% hint style="danger" %}
请每次编辑 **纹理**、**3D 模型**、**声音** 等后都使用 `/iazip`，然后 **重新上传** 包到 **DropBox** 并使用 **/iareload**，否则您将看不到任何更改。
{% endhint %}

{% hint style="warning" %}
**每次上传** 新版本的 **资源包** 时，请 **更改** **文件名** 以 **强制** 游戏 **重新下载** **新版本**。\
如果您 **重新上传** 相同的 **zip** 文件并保持 **相同的 URL**，则 **不会更新** 给每个玩家。
{% endhint %}

## 但这太慢了！我必须在 DropBox 上重新上传太多次！

是的，这就是为什么您应该使用自托管功能而不是 **DropBox**。但有些托管（便宜的那些）不提供端口开放，因此您必须使用 **DropBox**。

{% content-ref url="resourcepack-self-hosting.md" %}
[resourcepack-self-hosting.md](resourcepack-self-hosting.md)
{% endcontent-ref %}

## 如果需要继续安装

{% content-ref url="../../first-install.md" %}
[first-install.md](../../first-install.md)
{% endcontent-ref %}
