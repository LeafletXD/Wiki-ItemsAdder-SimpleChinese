---
描述: 如何安装插件
---

# ⚙️ 首次安装

{% hint style="info" %}
**您应该先在** 电脑上的 **测试服务器** 上按照此配置 **以避免错误** 和过多的重启... 玩家不喜欢服务器一直离线。\
完成此步骤后，您可以将文件上传到实际服务器。
{% endhint %}

{% hint style="danger" %}
**确保** 所有插件和服务器软件都是最新的！\

**检查** 您正在下载的ItemsAdder的版本!\
<mark style="color:red;">**V3 版本只可用于 1.20.4或更低的版本**</mark> <mark style="color:red;">**V4 版本只可用于 1.20.6或更高的版本**</mark>
{% endhint %}

## 步骤 1 - 安装插件和库（libraries）

* 使用 `/stop` 关闭服务器
* 安装 [**ProtocolLib**](https://ci.dmulloy2.net/job/ProtocolLib/lastSuccessfulBuild/)
* 安装 [**LoneLibs**](https://www.spigotmc.org/resources/lonelibs.75974/)
* 将 `ItemsAdder.jar` 文件放入plugins文件夹中
* 启动服务器
* 让 ItemsAdder 完成加载 **所有内容**

第一步完成。

{% hint style="warning" %}
现在你需要完成 **步骤 2** 来配置资源包（不要担心，只要跟随步骤一个一个设置就不会有事，不会很难）。\
<mark style="color:red;">**不要跳过！**</mark>
{% endhint %}

## 步骤 2 - 资源包首次安装

{% hint style="warning" %}
该步骤极其重要，如果你不完成该步骤，插件将 <mark style="color:red;">**不会正常工作！**</mark>
{% endhint %}

在使用插件之前，你需要决定资源包的托管方式。\
点击下方以选择资源包的托管方法（最佳方法：`self-host` 自托管）。

{% content-ref url="plugin-usage/resourcepack-hosting/" %}
[资源包托管](plugin-usage/resourcepack-hosting/)
{% endcontent-ref %}

## 步骤 3 - （可选）添加官方 ItemsAdder 自定义内容

![](.gitbook/assets/items\_showcase\_gif.apng)

**ItemsAdder** 附带了大量为您预先创建的自定义内容。\
这些内容不会自动包含在下载的插件中，因为有些人可能不希望每个物品/功能都自动添加到他们的服务器中。

### 默认包 (可选)

![](<.gitbook/assets/image (47).png>)

* 下载最新版本的 **DefaultPack**：[下载](https://github.com/ItemsAdder/DefaultPack/releases/latest)
* 将内容解压到 `ItemAdder` 文件夹中，并在提示时覆盖文件
* 运行 `/iazip` 命令（如果您不是使用 **self-host**，请按照您的 [资源包托管](plugin-usage/resourcepack-hosting/) 进行操作）。

### 其他包 (可选)

![](<.gitbook/assets/image (50).png>)

* 如果需要，您可以下载 **OtherPacks**，它提供了更多内容：[下载](https://github.com/ItemsAdder/OtherPacks/releases/latest)
* 将内容解压到 `ItemAdder` 文件夹中，并在提示时覆盖文件
* 运行 `/iazip` 命令（如果您不是使用 **self-host**，请按照您的 [资源包托管](plugin-usage/resourcepack-hosting/) 进行操作）。

如果您使用的是 1.17 或更低版本，您需要更改矿石生成设置：

* 打开以下文件并将 `enabled` 设置为 `true`：
  * `contents\iaalchemy\configs\worlds_populators_old.yml`
  * `contents\iasurvival\configs\ores\configs\worlds_populators_old.yml`
* 打开以下文件并将 `enabled` 设置为 `false`：
  * `contents\iaalchemy\configs\worlds_populators_1_18.yml`
  * `contents\iasurvival\configs\ores\configs\worlds_populators_1_18.yml`

### 删除默认物品 (可选)

{% content-ref url="broken-reference" %}
[删除ItemsAdder的默认物品](broken-reference)
{% endcontent-ref %}
