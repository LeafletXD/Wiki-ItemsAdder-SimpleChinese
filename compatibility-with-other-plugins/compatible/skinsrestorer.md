# SkinsRestorer

## [点击下载](https://www.spigotmc.org/resources/skinsrestorer.2124/)

## 如何修复进入游戏时资源包未应用的问题

### 步骤 1

安装 [**ResourcepackBroadcast**](https://www.spigotmc.org/resources/resourcepackbroadcast.88318/)

### 步骤 2

设置 **ResourcepackBroadcast** 的 `config.yml`，在资源包正确加载时执行 `sr applyskin` 命令：

```yaml
success:
  enabled: true
  message:
    enabled: true
    text: "&e%player_name% loaded resourcepack"
  placeholder:
    enabled: true
    text: "%img_smile%"
  commands:
    apply_skin:
      enabled: true
      command: sr applyskin %player_name%
      as_console: true
```

### 步骤 3

打开 **SkinsRestorer** 的 `config.yml` 文件，将 `DisableOnJoinSkins` 设置为 `false`

### 步骤 4

安装 [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)（如果还没有的话）。\
执行命令 `/papi ecloud download Player` 然后 `/papi reload`。

### 完成
