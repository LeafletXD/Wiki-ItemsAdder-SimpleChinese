# 无法在聊天栏打字和无法移动

## WorldGuard

如果你遇到载具出现问题（例如载具被卡在世界下方或出现其他奇怪的错误），请打开 WorldGuard 的 `config.yml` 文件并设置以下内容：

```
block-plugin-spawning: false
```

## Towny

{% hint style="warning" %}
如果你在使用 Towny 插件时遇到载具问题，请打开 Towny 的 `config.yml` 文件，并从以下配置中移除 **Slime**：
{% endhint %}

```yaml
town_mob_removal_entities: Monster,Flying,Shulker,SkeletonHorse,ZombieHorse
```

## Mob Farm Manager

如果你使用了 [Mob Farm Manager](https://www.spigotmc.org/resources/mob-farm-manager-supports-1-7-10-up-to-1-16-hopper-support.15127/) 插件，请检查是否为实体类型 **`SLIME`** 设置了任何规则，这可能会移除载具的一部分并导致出现该错误。

## Residence

在 **Residence** 内使用命令 `/res set monsters t/r`。\
我已经联系了 Residence 的开发者，希望[他们能解决这个问题](https://github.com/Zrips/Residence/issues/469#issuecomment-801425643)。

## 其他移除 / 分组 / 合并生物的插件

请移除对实体类型 **`SLIME`** 的任何分组、合并或移除功能。
