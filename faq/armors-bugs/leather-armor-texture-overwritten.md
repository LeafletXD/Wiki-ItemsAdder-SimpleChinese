# 皮革盔甲材质被覆盖

## 皮革盔甲图层纹理不断被 ItemsAdder 覆盖

![](<../../.gitbook/assets/image (45) (1) (1).png>)

ItemsAdder 会自动覆盖皮革盔甲图层纹理以创建自定义盔甲。  
自定义盔甲是通过彩色皮革制成的，但默认的 Minecraft 皮革盔甲纹理并不适合表现矿物质感。

在某些服务器中，你可能完全不需要此功能，并可能更希望使用原版皮革盔甲图层纹理，或者使用自己的自定义纹理。

## 如何禁用此功能？

{% hint style="warning" %}
此功能需要 ItemsAdder 2.5.2 及以上版本
{% endhint %}

要禁用此功能，只需在 ItemsAdder 的 `config.yml` 文件中设置以下选项，并再次运行 `/iazip`（如有需要，请重新[托管资源包](../../plugin-usage/resourcepack-hosting/)）。

{% code title="config.yml" %}
```yaml
disable-overwrite-leather-armor-layers-textures: true
```
{% endcode %}
