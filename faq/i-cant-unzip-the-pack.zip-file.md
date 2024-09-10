# 📤 我不能解压pack.zip文件

禁用保护选项。

{% code title="config.yml" %}
```yaml
  zip:
    protect-file-from-unzip:
      enabled: false
      extreme: false
```
{% endcode %}

{% hint style="danger" %}
这是保护 ZIP 文件不被解压的选项。\
在禁用此选项时请小心，如果你不保护它，任何人都可以解压你的文件。
{% endhint %}
