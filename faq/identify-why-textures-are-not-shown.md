# 🔍 资源包未正确加载

{% hint style="danger" %}
#### 请在请求支持之前仔细阅读此页面。

大多数情况下，通过阅读此页面可以轻松解决问题。
{% endhint %}

## 何时阅读此页面

* 资源包根本没有加载
* 玩家加入时显示全屏错误
* 显示黑色和紫色纹理
* 模型未正确加载
* 资源包加载失败
* 自定义声音未播放
* 资源包一直加载故障

{% hint style="warning" %}
#### auto-external-host

如果你仍在使用 `auto-external-host`，需要更改托管方法，因为它已经不再有效。\
[更多信息请点击这里](../old/old-guides/automatic-upload-hosting.md)
{% endhint %}

## 如何阅读服务器日志

* 运行命令 `/iazip`
* 等待完成
* 阅读你的服务器控制台或使用任何文本编辑器（例如 VSCode）打开文件 `logs/latest.log`
* 检查是否有错误或警告，并仔细阅读，它们通常包含有用的信息

## 如何阅读客户端日志（不是服务器日志）

{% hint style="warning" %}
当出现故障时，建议使用原版客户端。\
游戏提供的日志通常会在需要时被支持团队要求。\
简洁的日志更有助于支持你并更容易找到解决方案。
{% endhint %}

### 任意启动器

加入服务器并让资源包加载。\
打开你的 Minecraft 游戏日志文件，**不是服务器** 日志。\
通常位于：`%appdata%\.minecraft\logs\latest.log` \
你可以清楚地看到哪些文件加载失败以及原因，大多数情况下错误信息很明确。

### 原版启动器

#### 启用输出日志

![](../.gitbook/assets/image\_\(135\).png)

#### 加入服务器并阅读日志

![](<../.gitbook/assets/json_errors (1) (1) (1) (1).png>)

#### 查找哪个文件出现问题

你可以清楚地看到哪些文件加载失败以及原因，大多数情况下错误信息很明确。\
在此示例中，我有两个损坏的文件 `gem_vending_machine` 和 `whitebathroom_sink`。\
错误信息告诉我 JSON 文件已损坏，它们可能包含错误字符或已被破坏。

## 资源包未加载，我收到错误 <a href="#resourcepack-not-loading-i-get-an-error-in-chat" id="resourcepack-not-loading-i-get-an-error-in-chat"></a>

* 如果你有 **SkinsRestorer**，请[阅读此处](../compatibility-with-other-plugins/compatible/skinsrestorer.md)。
* 检查是否有其他插件使用 **自定义资源包**\
  如果你有类似插件，请 **禁用** 其 **资源包** 功能，否则 **ItemsAdder** 将无法正确应用资源包。如果你想同时应用两个资源包，请[阅读此处](../plugin-usage/merge-resourcepacks/)。
* 确保 `server.properties` 文件中没有设置任何资源包。
* **Minecraft** 限制服务器资源包的 **大小**，**1.14** 版本为 **50MB**，**1.15+** 版本为 **100MB**，**1.18+** 版本为 **250MB**。\
  在创建 ZIP 文件之前，请确保 **压缩** 你的 **纹理** 和 **音乐** 文件。
* 确保你的 `url` 是指向 ZIP 文件的 **直接** 下载链接。\
  如果你在浏览器（Firefox/Chrome）中粘贴链接，你应该会立即看到下载开始。\
  如果你看到带有按钮的下载页面，则 URL 是错误的。\
  请查看资源包 [托管教程](../plugin-usage/resourcepack-hosting/)。
* 确保按照所有资源包托管 [教程](../plugin-usage/resourcepack-hosting/) 步骤操作。
* 如果你使用 [`自托管`](../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md)，请确保端口已打开。
* 运行 `/iainfo` 命令，确保资源包 **URL** 可以从浏览器访问，并且直接下载资源包 `.zip` 文件。
* 确保你在项目 **名称**、**命名空间**、**纹理** 文件（png）和 **模型** 文件（json）中未使用 **大写字母**、**空格** 或 **特殊字符**。\
  例如，自定义物品的 ID：`CustomSword` 是错误的，使用 `custom_sword`。

### _我的玩家无法加载资源包！我已经按照整个教程操作_ <a href="#my-players-cant-see-textures-but-ive-followed-the-whole-tutorial" id="my-players-cant-see-textures-but-ive-followed-the-whole-tutorial"></a>

* 在服务器列表设置中启用资源包：[http://imgur.com/a/SG0AU](http://imgur.com/a/SG0AU)
* 确保玩家加入时没有打开任何物品栏（GUI）或书本。\
  这可能导致资源包提示消失，玩家无法点击。\
  为解决此问题，你可以使用免费的插件 [ResourcePackBroadcast](https://www.spigotmc.org/resources/resourcepackbroadcast.88318/)。\
  这允许你在资源包被接受后立即运行命令（以及其他各种功能）。
* 将 **ItemsAdder** 中 `config.yml` 的 `delay-ticks` 增加到 `10` 或更高。
* 离开服务器，转到 `%appdata%/.minecraft/server-resource-packs` 并删除所有内容。然后再次加入服务器。
