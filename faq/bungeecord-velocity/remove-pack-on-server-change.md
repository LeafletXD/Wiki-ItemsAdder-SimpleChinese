# 切换服务器时移除资源包

## 当玩家切换服务器时移除资源包

如果你有多个服务器，并希望用户在切换服务器时移除 ItemsAdder 的资源包，请按照本教程进行操作。

### 如何操作

1. 下载 [空白资源包](http://matteodev.it/spigot/itemsadder/blank\_pack.zip)。
2. 将其上传到某个地方，例如（跳过教程中的 `/iazip` 部分）[DropBox](../../plugin-usage/resourcepack-hosting/resourcepack-on-dropbox.md)、[OneDrive](../../plugin-usage/resourcepack-hosting/onedrive.md)、[GoogleDrive](../../plugin-usage/resourcepack-hosting/google-drive-1.17.1+.md) 等。
3. 获取该 URL。
4. 打开其他服务器的 `server.properties` 文件，并设置该 URL。

{% code title="server.properties" %}
```properties
resource-pack=http://your_url/blank_pack.zip
```
{% endcode %}

完成！

当玩家加入你的其他服务器时，ItemsAdder 资源包将被默认的资源包替换。
