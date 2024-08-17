# CMI
## Ranks

1. 打开你 CMI 文件夹中的 `Settings/Chat.yml` 文件，将 `GeneralFormat`（我使用 `%vault_prefix%` 占位符代替 CMI 的 `{prefix}`）设置为：

```yaml
GeneralFormat: '%vault_prefix% &f{displayName}&7: &r{message}'
```

2. 下载 [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) 和 [Vault](https://github.com/MilkBowl/Vault/releases/latest)。\
3. 安装它们并重启你的服务器。\
4. 输入 `/papi ecloud download Vault`。\
5. 最后，输入 `/papi reload`。

现在，ItemsAdder 应该可以正常与 CMI 的聊天功能兼容。
