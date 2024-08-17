# Authme

## [点击下载](https://www.spigotmc.org/resources/authmereloaded.6269/)

## 如何在登录后应用资源包

打开 **ItemsAdder** 的 **config.yml** 文件，禁用 `apply-on-join`。

```yaml
resource-pack:
  apply-on-join: false
```

打开 **Authme** 的 `commands.yml` 文件，将 `onLogin` 修改为：

```yaml
onLogin:
  apply_pack:
    command: 'iatexture %p'
    executor: CONSOLE
```

{% hint style="warning" %}
确保配置文件中只有 **一个 onLogin 设置**。
{% endhint %}
