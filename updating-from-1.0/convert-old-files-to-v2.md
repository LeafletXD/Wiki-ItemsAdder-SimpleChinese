# 将旧数据转换为v2版本



{% hint style="danger" %}
**建议启动一个全新的世界，而不要使用旧世界，因为转换器虽然有效，但仍处于实验阶段。**
{% endhint %}

{% hint style="warning" %}
## 如果您没有创建任何自定义物品，只使用了我的自定义物品，请跳过该教程，您无需转换文件。但请务必按照教程“在游戏中转换旧物品”进行操作。

您只需将 ItemsAdder 文件夹重命名为 ItemsAdder_backup，删除旧插件，然后安装 2.0 版本。
{% endhint %}

### 有什么变化？

ItemsAdder v2 是对之前版本的全面重构。它更改了每个配置文件和每个资源包的文件路径/属性/格式。\
这就像是一个全新的插件，拥有更多功能、优化更佳且更易于维护。

### 如何将旧配置文件和资源包转换为新格式？

您需要按照这个教程进行操作 :D

{% hint style="warning" %}
**请务必仔细遵循教程**，不要急于操作，否则可能会犯错，导致转换过程花费更长时间！
{% endhint %}

{% hint style="danger" %}
强烈建议在您电脑上的本地测试服务器上进行此操作，以避免犯错和数据丢失的风险！O-O
{% endhint %}



## 步骤 1

* 关闭服务器并删除旧版本 ItemsAdder.jar
* 下载[ItemsAdder Converter ](https://www.spigotmc.org/resources/itemsadder-converter.75952/)并放入plugins文件夹中

## 步骤 2 - 复制物品配置

* 打开服务器的 **plugins** 文件夹，并创建一个名为 **ItemsAdder_old** 的 **新** 文件夹。
* 打开您的 **旧** ItemsAdder 文件夹，并从 `items` 文件夹中复制文件 **（参见截图）**。

![](<../.gitbook/assets/image (6).png>)

* 将 **items** 文件夹粘贴到 **ItemsAdder_old** 文件夹中。

![](<../.gitbook/assets/image (5).png>)

## 步骤 3 - 复制资源包

* 在 **ItemsAdder_old** 文件夹中创建一个名为 **pack** 的 **新** 文件夹
* 将旧资源包 **.zip** 文件的 **确切内容** 解压到新创建的 **pack** 文件夹中

![](../.gitbook/assets/image.png)

## 步骤 4 - 准备新版本的 ItemsAdder 2.0

{% hint style="info" %}
**如果您不需要我的自定义物品，只想创建自己的物品：**

打开 **ItemsAdder** 文件夹中（由 **ItemsAdder 2.0** 版本刚生成的） `config.yml` 文件，并将以下属性设置为 `false`。

```
extract-default-items: false
extract-default-resources: false
```

然后删除 `ItemsAdder\data\items_packs\...` 文件夹中的所有文件夹 **但保留** `minecraft` 文件夹。\
同时，删除 `ItemsAdder\data\resource_pack\assets\...` 文件夹中的所有文件夹 **但保留** `minecraft` 文件夹。

您还需要从 `ia_gui.yml` 中移除我的分类。
{% endhint %}

## 步骤 5 - 准备转换器

{% hint style="success" %}
ItemsAdder 转换器会自动跳过我的自定义物品，因此它将创建一个只包含您自己创建的物品的包。
{% endhint %}

#### 在开始转换之前进行配置

* 打开文件 `plugins/ItemsAdderConverter/config.yml`
* 编辑 `namespace` 为自定义名称。您可以选择服务器名称或任何您想要的名称。例如，我的一些物品的 **namespace** 是 "`itemsadder`"，因此您可以使用像 ` /iaget itemsadder:ruby` 这样的命令（但如您所见，我在新插件中创建了更多的命名空间，以便分离功能）。

## 步骤 6 - 转换

要开始转换：

* 启动服务器
* 等待服务器完成加载所有内容
* 使用命令 `/itemsadderconverter:iaconvert`
* **等待** 转换 **完成**
* 检查是否出现任何错误
* **仅在** 转换 **完成后** 停止服务器

## 安装 ItemsAdder v2

{% hint style="danger" %}
* **停止** 服务器
* 请确保您 **删除了旧的 ItemsAdder.jar**
* 如果插件文件夹中仍有旧的 ItemsAdder 文件夹，请 **重命名** 为 **ItemsAdder_backup**，或者如果已有备份则 **删除** 它。
* **下载** ItemsAdder 2.0 并将其放入您的插件文件夹中
* **启动** 服务器
* 等待 ItemsAdder 2.0 完成文件创建
* 如果出现任何错误，请阅读错误信息并检查是否做错了什么（缺少依赖项、错误的 Spigot 版本等），然后重试此步骤。
* （如果出现有关资源包 URL 的错误，可以忽略，这是正常的，您稍后将配置它）
* 打开刚刚创建的 **ItemsAdder_converted** 文件夹
* 将两个文件夹 `items_packs` 和 `resource_pack` 复制到新的 `ItemsAdder` 文件夹中（如有提示，请替换任何文件）
* **重启** 服务器
{% endhint %}

## 最后任务

* 删除 `ItemsAdderConverter`、`ItemsAdder_converted` 和 `ItemsAdder_old` 文件夹。
* 删除 `ItemsAdderConverter.jar`

## 资源包配置

请按照这个简短的教程来激活资源包：

{% content-ref url="../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md" %}
[自托管](../plugin-usage/resourcepack-hosting/resourcepack-self-hosting.md)
{% endcontent-ref %}



****
