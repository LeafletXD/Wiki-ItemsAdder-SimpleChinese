# 🔖 自定义头衔材质 (前缀)

## 自定义头衔材质

![](<../../.gitbook/assets/image (27) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (3).png>)

{% hint style="warning" %}
**您必须使用** [**LuckPerms**](https://www.spigotmc.org/resources/luckperms.28140/) **和** [**TAB**](https://www.mc-market.org/resources/14009/) **来按照本教程进行操作，如果您使用其他权限和TAB插件，方法可能会有所不同。**

**如果您使用其他前缀插件，您可能需要使用** [**此方法**](font-images/using-font\_images-everywhere.md) **来显示头衔**
{% endhint %}

## 如何创建我的头衔？

### 在这里下载示例头衔

{% embed url="https://www.spigotmc.org/resources/ranks-betterranks-with-custom-textures-for-itemsadder.84852/" %}

### 创建新的头衔配置

打开 `ItemsAdder/contents/betterranks/configs/ranks.yml` 文件，**复制**并**粘贴**其中一个头衔配置。\
然后将其重命名为您的头衔，同时决定新的 **.png** 文件名，例如 `custom`

```yaml
  custom:
    permission: "ranks.custom"
    show_in_gui: true
    suggest_in_command: false
    path: "custom.png"
    scale_ratio: 9
    y_position: 8
```

{% hint style="warning" %}
不要更改 `scale_ratio` 和 `y_position`。这样会使头衔看起来像素化。
{% endhint %}

### 创建PNG图像

**复制**我的头衔 **.png** 文件并在文件夹 `contents/betterranks/textures/` 中编辑它。\
\
您可以使用 **Photoshop**、**GIMP**、**Paint.NET** 或任何其他您使用的编辑软件进行编辑。\
例如，复制 `admin.png`，将其命名为 `custom.png` 并进行编辑。

{% hint style="danger" %}
**不要更改头衔图像的高度！** \
**只更改宽度，否则图像会看起来像素化！**
{% endhint %}

### 示例：

例如，为了制作一个类似于我的 **BetterRanks** 附加组件的头衔，您只需使用 [Minecraftia](https://www.dafont.com/andrew-tyler.d2526) 字体并剪切一些像素。

![](<../../.gitbook/assets/image (36).png>)

![](<../../.gitbook/assets/image (37).png>)

![](<../../.gitbook/assets/image (38).png>)

![](<../../.gitbook/assets/image (39).png>)

## 在游戏中使用头衔

### Luckperms

#### 创建一个组，例如（管理员）

使用此命令 `/lp creategroup admin`

#### 添加前缀

使用此命令获取编辑器：`/lp editor`\
现在单击链接并打开网页编辑器。

选择角色，此例中为 `admin`。

![](<../../.gitbook/assets/image (77).png>)

在底部输入框中写入 `prefix.100.`，后跟前缀占位符，此例中我将使用 `:admin:`

`prefix.100.:admin:`（确保您正确写入）。

![](<../../.gitbook/assets/image (80) (1).png>)

按 <mark style="color:green;">**`+添加`**</mark>

![](<../../.gitbook/assets/image (74) (1).png>)

如您所见，权限列表中有新行，这是前缀设置。

![](<../../.gitbook/assets/image (70).png>)

现在保存您的更改

![](<../../.gitbook/assets/image (44).png>)

#### 将组分配给玩家

使用此命令（将 `LoneDev` 更改为您的玩家名称） `/lp user LoneDev group add admin`

![](../../.gitbook/assets/image\_\(40\).png)

### TAB插件

{% hint style="warning" %}
确保您已安装 [PlaceholderAPI](font-images/using-font\_images-everywhere.md)
{% endhint %}

#### 编辑TAB插件的config.yml

**在 `groups` 类别下添加**这一部分，或者如果已经存在则编辑它。\
（您必须使用 `%img_admin%` 而不是 `:admin:`，因为 **TAB** 只识别 **PlaceholderAPI** 占位符，而不是 **ItemsAdder** 占位符。此规则对 **其他插件** 也有效）

```yaml
  Admin:
    tabprefix: '%img_admin%  '
    tagprefix: '%img_admin%  '
```

然后使用命令 `/tab reload`

![](../../.gitbook/assets/image\_\(38\).png)

![](../../.gitbook/assets/image\_\(39\).png>)
