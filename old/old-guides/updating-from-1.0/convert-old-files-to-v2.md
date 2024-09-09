# 将旧数据转换为v2版本

{% hint style="danger" %}
**建议创建一个全新的世界，不要使用旧世界，尽管转换工具可以工作，但它们仍处于实验阶段。**
{% endhint %}

{% hint style="warning" %}
#### 如果您没有创建任何自定义物品并且只使用我的自定义物品，请跳过本教程，您不需要转换文件。但请确保按照教程“在游戏中转换旧物品/方块”操作。

您只需将 ItemsAdder 文件夹重命名为 ItemsAdder\_backup，删除旧插件并安装 2.0 版本。
{% endhint %}

### 有什么变化？

ItemsAdder v2 是对之前版本的完全重写。它更改了所有配置和资源包文件的路径/属性/格式。\
这是一个全新的插件，具有更多功能、更高的优化，且更易于维护。

### 如何将旧的配置文件和资源包转换为新格式？

请按本教程进行操作 :D

{% hint style="warning" %}
**请务必仔细遵循教程**，不要匆忙操作，否则可能出错，导致转换时间更长。
{% endhint %}

{% hint style="danger" %}
此操作仅在您的本地测试服务器上进行，以避免错误并防止数据丢失。
{% endhint %}

## 第一步

* 从您的测试服务器中禁用旧的 ItemsAdder 插件（删除 ItemsAdder.jar 并停止服务器）
* 下载 [ItemsAdder Converter](https://www.spigotmc.org/resources/itemsadder-converter.75952/)，并将其放入测试服务器的插件文件夹中。

## 第二步 - 复制物品配置

* 打开服务器的 **plugins** 文件夹，创建一个 **新** 文件夹，命名为 **ItemsAdder\_old**
* 打开您的 **旧** ItemsAdder 文件夹，复制物品文件夹中的文件 **(见截图)**

![](<../../../.gitbook/assets/image (1) (1) (1) (1) (1).png>)

* 将 **items** 文件夹粘贴到 **ItemsAdder\_old** 文件夹中

![](<../../../.gitbook/assets/image (4) (1) (1).png>)

## 第三步 - 复制资源包

* 在 **ItemsAdder\_old** 文件夹中创建一个 **新** 文件夹，命名为 **pack**
* 将旧资源包 **.zip** 文件的 **内容** 提取到新文件夹 **pack** 中

![](<../../../.gitbook/assets/image (2) (1) (1).png>)

## 第四步 - 准备 ItemsAdder 2.0

{% hint style="info" %}
**如果您不关心我的自定义物品，只想创建自己的物品：**

打开 **ItemsAdder** 文件夹中的 `config.yml`（刚由 **ItemsAdder 2.0** 版本生成），将以下属性设置为 false。

```
extract-default-items: false
extract-default-resources: false
```

然后删除 `ItemsAdder\data\items_packs\...` 文件夹中的所有文件夹，**保留** `minecraft` 文件夹。\
并删除 `ItemsAdder\data\resource_pack\assets\...` 文件夹中的所有文件夹，**保留** `minecraft` 文件夹。

还需要从 `ia_gui.yml` 中删除我的类别。
{% endhint %}

## 第五步 - 准备转换器

{% hint style="success" %}
ItemsAdder 转换器会自动跳过我的自定义物品，因此它将创建一个仅包含您自定义物品的包。
{% endhint %}

#### 在开始转换之前配置

* 打开文件 `plugins/ItemsAdderConverter/config.yml`
* 将 `namespace` 编辑为一个自定义名称。您可以选择服务器名称或其他任何名称。例如，我的一些物品具有 **namespace** "`itemsadder`"，因此您将能够使用 `/iaget itemsadder:ruby` 命令（不过，您会注意到我在新插件中创建了更多的命名空间，以便分离不同功能）。

## 第六步 - 转换

开始转换：

* 启动服务器
* 等待其加载完毕
* 使用命令 `/itemsadderconverter:iaconvert`
* **等待** 它**完成**
* 检查是否有任何错误
* **仅在**转换完成后**停止**服务器。

## 安装 ItemsAdder v2

{% hint style="danger" %}
* **停止**服务器
* 请确保您**删除了旧的 ItemsAdder.jar**
* 如果插件中仍有旧的 ItemsAdder 文件夹，请将其**重命名**为 **ItemsAdder\_backup** 或**删除**它（如果您已经有备份的话）。
* **下载** ItemsAdder 2.0 并将其放入插件文件夹中
* **启动**服务器
* 等待 ItemsAdder 2.0 完成文件创建
* 如果遇到任何错误，请检查并确认是否有依赖缺失或使用了错误的 Spigot 版本，然后重试此步骤。
* （忽略有关资源包 URL 的错误提示，这很正常，稍后会进行配置）
* 打开刚刚创建的 **ItemsAdder\_converted** 文件夹
* 将两个文件夹 `items_packs` 和 `resource_pack` 复制到新的 `ItemsAdder` 文件夹中（如果有提示，请替换文件）
* **重启**服务器
{% endhint %}

## 最后步骤

* 删除 `ItemsAdderConverter`、`ItemsAdder_converted`、`ItemsAdder_old` 文件夹。
* 删除 `ItemsAdderConverter.jar`。

## 资源包配置

请按照以下快速教程激活资源包：

{% content-ref url="../../../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md" %}
[自托管](../../../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md)
{% endcontent-ref %}

***
