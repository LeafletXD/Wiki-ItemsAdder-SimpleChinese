# 📤 用OneDrive托管

{% hint style="warning" %}
#### 不推荐使用
{% endhint %}

（翻译者：我**强烈不建议**使用该方法作为第三方托管，因为国内可能会出现墙或是下载过慢，建议使用**自托管**或是寻找其他稳定的文件托管平台，我用过Github和Gitee）

### 第一步

![](<../../.gitbook/assets/image (52) (1) (1) (1) (1).png>)

### 第二步

![](<../../.gitbook/assets/image (43) (1) (1).png>)

### 第三步

![](<../../.gitbook/assets/image (53) (1) (1).png>)

### 第四步

打开 **ItemsAdder** 的 `config.yml` 并为您的新 URL 启用 `external-host` 选项。

{% code title="config.yml" %}
```yaml
    external-host:
      enabled: true
      url: 'https://onedrive.live.com/yoururl.....'
      skip-url-file-type-check___DONT_ASK_HELP_IF_SET_TRUE: true
```
{% endcode %}

这非常重要。将其设置为 true。

```yaml
skip-url-file-type-check___DONT_ASK_HELP_IF_SET_TRUE: true
```

{% hint style="warning" %}
请注意，这有点“风险”，因为服务器无法确保 URL 的有效性。

如果 URL 无效或 OneDrive 未提供直接下载，这可能会导致您的玩家在登录阶段被卡住，有时会发生这种情况。
{% endhint %}

## 如果需要继续安装

{% content-ref url="../../first-install.md" %}
[first-install.md](../../first-install.md)
{% endcontent-ref %}
