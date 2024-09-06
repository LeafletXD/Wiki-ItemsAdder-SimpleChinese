# ModelEngine

## [点击下载](https://www.spigotmc.org/resources/conxeptworks-model-engine%E2%80%94ultimate-entity-model-manager-1-14-1-17-1.79477/)

（[免费演示版本](https://www.spigotmc.org/resources/conxeptworks-model-engine-demo-1-16-5-1-19-4.106521/)）

## 如何添加兼容性？

<details>

<summary>点击查看适用于 ItemsAdder 3.4.1-r4 及以下版本的旧方法</summary>

* 将所有的怪物模型和配置文件放入 **ModelEngine** 插件文件夹中（有关更多信息，请阅读 **ModelEngine** 教程）。
* 运行 `/meg reload` 生成 **ModelEngine** 资源包。
* 打开 `plugins/ModelEngine/resource_pack/assets/` 文件夹。
* 将 `assets` 文件夹复制到 `plugins/ItemsAdder/contents/modelengine/resourcepack/` 文件夹中。
* 运行 `/iazip`（如果需要，请参阅 [资源包托管教程](../../plugin-usage/resourcepack-hosting/)）。

</details>

* 将所有的怪物模型和配置文件放入 **ModelEngine** 插件文件夹中（有关更多信息，请阅读 **ModelEngine** 教程）。
* 打开 **ItemsAdder** 的 `config.yml` 文件，并设置如下：

```yaml
    merge_other_plugins_resourcepacks_folders:
      - "ModelEngine/resource pack"
```

* 运行 `/meg reload` 生成 **ModelEngine** 资源包。
* 运行 `/iazip`（如果需要，请参阅 [资源包托管教程](../../plugin-usage/resourcepack-hosting/)）。

## ItemsAdder 与 ModelEngine 之间的区别

<details>

<summary>点击查看 Ticxo 提供的旧版比较</summary>

[点击这里](https://git.lumine.io/mythiccraft/modelengine/-/wikis/Comparison:-ItemsAdder) 访问旧版比较页面。

<mark style="color:red;">⚠️</mark> 该比较页面自 2022 年 11 月 26 日以来未更新，可能无法反映插件的实际状态。

</details>

### 免责声明

此页面旨在不抨击 ModelEngine 的工作成果，也不决定哪个插件更好。\
ModelEngine 允许您引入几乎与原版相同的自定义实体，价格合理。\
这些只是我对 ModelEngine 的看法，但可能有些功能我遗漏了。\
因此，请以一定的保留态度看待我的观点，并询问其他人他们更喜欢哪个插件。

{% hint style="warning" %}
如果您发现此页面上有不正确的数据，请考虑联系我。我很乐意讨论并修复报告的差异。
{% endhint %}

***

<table><thead><tr><th width="239.33333333333331">功能</th><th width="173">ItemsAdder</th><th>ModelEngine v3</th><th>ModelEngine v4</th></tr></thead><tbody><tr><td>动画过渡</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>异步<br>(TPS 不受影响)</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Blockbench 插件</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Citizens 集成</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>社区制作的资源</td><td>约 20</td><td>约 200</td><td>?</td></tr><tr><td>可配置的着色项</td><td>❌<br>(默认是药水)</td><td>✅<br>(默认是皮革马具)<br>(所有皮革盔甲（头盔除外）、所有药水、箭矢和填充地图)</td><td>与 MEG v3 相同</td></tr><tr><td>费用</td><td>€19.95</td><td><p>v3: $18.99<br></p><p>（需要付费更新 v3->v4）</p></td><td><p>v4: $31.99</p><ul><li>比 ItemsAdder 贵 52%</li><li>比 MEG v3 贵 72%<br></li></ul></td></tr><tr><td>效果关键帧<br>(粒子和声音效果的关键帧)</td><td>✅</td><td>✅*<br>(<a href="https://github.com/Ticxo/Model-Engine-Wiki/wiki/[Temporary-Wiki]-3.0-Features#scriptable-keyframes">可脚本化的关键帧</a>)</td><td>未知</td></tr><tr><td>手持物品显示</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>头部位置</td><td>必须居中</td><td>可以在任何位置</td><td>与 MEG v3 相同</td></tr><tr><td>逆向运动学</td><td>❌</td><td>✅*<br>(仅限分段)</td><td>与 MEG v3 相同</td></tr><tr><td>缩放关键帧</td><td>✅</td><td>❌</td><td>✅</td></tr><tr><td>模型伪装</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>无限骨骼模型尺寸限制</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>玩家皮肤骨骼</td><td>✅*<br>(仅在表情中)</td><td>❌</td><td>✅</td></tr><tr><td>显示实体支持</td><td>❌</td><td>❌</td><td>✅</td></tr><tr><td>模型导入</td><td>使用自定义 Blockbench 插件进行导入和导出</td><td>拖放</td><td>与 MEG v3 相同</td></tr><tr><td>实体旋转<br>(身体和头部骨骼互动)</td><td>与原版实体完全相同</td><td>玩家和实体风格+<br>[玩家] 当头部-身体角度过大时身体旋转<br>[实体] 身体在一定延迟后旋转<br>模型面向运动方向<br>可配置稳定角度、夹紧角度、旋转持续时间和延迟<br>不对称夹紧</td><td>与 MEG v3 相同</td></tr><tr><td>多名牌</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>多碰撞箱</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>MythicMobs 集成</td><td>6 种机制（1 种机制但做 6 件事）：<br>- 应用模型<br>- 播放和停止动画<br>- 覆盖默认动画<br>- 骑乘和卸下模型<br>- 为模型上色和附魔<br>- 显示和隐藏骨骼<br><a href="../../plugin-usage/adding-content/mobs/advanced-method/mythicmobs.md">更多信息</a></td><td>30+ 种机制<br>- 应用和移除模型<br>- 播放和停止动画<br>- 覆盖默认动画<br>- 骑乘和卸下模型<br>- 设置、显示和隐藏名牌<br>- 为模型上色和附魔<br>- 伪装和解除伪装玩家<br>- 组合、移除、显示和隐藏骨骼<br>- 骨骼父子交换<br>- 创建雕像<br>- 高级多碰撞箱配置<br>- 即时模型变体切换<br>- 10+ 种特效相关机制</td><td>未知（需要检查）</td></tr><tr><td>非实体模型相关功能</td><td>✅（这是一个内容管理器，它允许添加的不仅仅是自定义实体）</td><td>❌（仅允许将自定义实体添加到游戏中）</td><td>与 MEG v3 相同</td></tr><tr><td>数据包数量</td><td>在某些情况下使用更少的数据包，在其他情况下使用更多的数据包。</td><td>在某些情况下使用更少的数据包，在其他情况下使用更多的数据包。</td><td>在某些情况下使用更少的数据包，在其他情况下使用更多的数据包。</td></tr><tr><td>过程动画<br>(实时计算)</td><td>❌</td><td>✅</td><td>✅</td></tr><tr><td>资源包生成</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>多个资源包</td><td>✅</td><td>❌</td><td>❌</td></tr><tr><td>稳定性</td><td>实体系统于 2022 年 3 月发布</td><td>于 2020 年 6 月 13 日发布</td><td>于 2023 年 10 月 1 日发布</td></tr><tr><td>特效模型<br>(用于投射物的轻量级模型)</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### 网络流量比较

这是对两个插件的网络流量使用情况的比较（较低的 **rx** 和 **traffic** 更好）。\
为了进行这些测试，我使用了 25 个 `ninja_skeleton` 模型，可从以下链接下载：[ItemsAdder](https://www.spigotmc.org/resources/entity-ninja-skeleton-for-itemsadder.100468/)、[ModelEngine](https://mythiccraft.io/index.php?resources/modelengine-ninja-skeleton-model.214/)。

#### 无 AI（静止状态下带有空闲动画）

<table><thead><tr><th width="96">插件</th><th width="90">版本</th><th width="90">模式</th><th width="91">包</th><th width="83">rx</th><th width="104">流量</th><th>视频</th></tr></thead><tbody><tr><td>IA</td><td>3.6.2</td><td>流畅</td><td>是</td><td>5500</td><td>300KiB/s</td><td><a href="https://youtu.be/lPHtIqBwx68">观看</a></td></tr><tr><td>IA</td><td>3.6.2</td><td>流畅</td><td>否</td><td>6800</td><td>160KiB/s</td><td><a href="https://youtu.be/-_GZ_SALruQ">观看</a></td></tr><tr><td>MEG</td><td>R3.1.9</td><td>A,A,C</td><td>-</td><td>8200</td><td>200KiB/s</td><td><a href="https://youtu.be/IuIxMatqSYo">观看</a></td></tr><tr><td>MEG</td><td>R4.0.2</td><td>-</td><td><em>是</em></td><td>8500</td><td>260KiB/s</td><td><a href="https://youtu.be/r4fbzi_sQgc">观看</a></td></tr></tbody></table>

<table><thead><tr><th width="198">IA</th><th width="151">MEG</th><th width="142">rx 差异 (a->b)</th><th>流量差异 (a->b)</th></tr></thead><tbody><tr><td>IA 3.6.2 包</td><td>MEG 3.1.9</td><td><mark style="background-color:green;">-49%</mark></td><td><mark style="background-color:red;">+33%</mark></td></tr><tr><td>IA 3.6.2</td><td>MEG 3.1.9</td><td><mark style="background-color:green;">-20%</mark></td><td><mark style="background-color:green;">-25%</mark></td></tr><tr><td>IA 3.6.2 包</td><td>MEG 4.0.2</td><td><mark style="background-color:green;">-54%</mark></td><td><mark style="background-color:red;">+13%</mark></td></tr><tr><td>IA 3.6.2</td><td>MEG 4.0.2</td><td><mark style="background-color:green;">-25%</mark></td><td><mark style="background-color:green;">-62%</mark></td></tr><tr><td>MEG 4.0.2</td><td>MEG 3.1.9</td><td><mark style="background-color:red;">+3%</mark></td><td><mark style="background-color:red;">+23%</mark></td></tr></tbody></table>

#### 有 AI（四处游荡）

<table><thead><tr><th width="98">插件</th><th width="90">版本</th><th width="90">模式</th><th width="87">包</th><th width="83">rx</th><th width="104">流量</th><th>视频</th></tr></thead><tbody><tr><td>IA</td><td>3.6.2</td><td>流畅</td><td>是</td><td>7700</td><td>450KiB/s</td><td><a href="https://youtu.be/Jow0Vhs2BSQ">观看</a></td></tr><tr><td>IA</td><td>3.6.2</td><td>流畅</td><td>否</td><td>13k</td><td>350KiB/s</td><td><a href="https://youtu.be/NiJRDJcVLTg">观看</a></td></tr><tr><td>MEG</td><td>R3.1.9</td><td>A,A,C</td><td>否</td><td>10k</td><td>270KiB/s</td><td><a href="https://youtu.be/1S5TXngOr0U">观看</a></td></tr><tr><td>MEG</td><td>R4.0.2</td><td>-</td><td><em>是</em></td><td>9000</td><td>280KiB/s</td><td><a href="https://youtu.be/yz1ZuTvFBEg">观看</a></td></tr></tbody></table>

<table><thead><tr><th width="198">IA</th><th width="151">MEG</th><th width="142">rx 差异 (a->b)</th><th>流量差异 (a->b)</th></tr></thead><tbody><tr><td>IA 3.6.2 包</td><td>MEG 3.1.9</td><td><mark style="background-color:green;">-23%</mark></td><td><mark style="background-color:red;">+66%</mark></td></tr><tr><td>IA 3.6.2</td><td>MEG 3.1.9</td><td><mark style="background-color:red;">+30%</mark></td><td><mark style="background-color:red;">+29%</mark></td></tr><tr><td>IA 3.6.2 包</td><td>MEG 4.0.2</td><td><mark style="background-color:green;">-14%</mark></td><td><mark style="background-color:red;">+60%</mark></td></tr><tr><td>IA 3.6.2</td><td>MEG 4.0.2</td><td><mark style="background-color:red;">+44%</mark></td><td><mark style="background-color:red;">+25%</mark></td></tr><tr><td>MEG 4.0.2</td><td>MEG 3.1.9</td><td><mark style="background-color:green;">-11%</mark></td><td><mark style="background-color:red;">+3%</mark></td></tr></tbody></table>

### 动画质量比较

{% tabs %}
{% tab title="itemsAdder" %}
{% embed url="https://youtu.be/uQHvIv7-laM" %}
{% endtab %}

{% tab title="ModelEngine" %}
{% embed url="https://youtu.be/ejhiwHn2fOM" %}
{% endtab %}
{% endtabs %}

### ModelEngine v4 “整体网络负载减少”争议

MythicCraft [公告](https://web.archive.org/web/20231020161618/https://mythiccraft.io/index.php?threads/modelengine-4-is-out-now.23407/) 宣传其新版本 ModelEngine v4 实现了“整体网络负载减少”。

在 MythicCraft 的 Discord 服务器上，有一些讨论称，与 MEG 3 相比，rx（发往客户端的数据包）极低。我也有用户联系我讨论这个问题，这引起了我的好奇。\
然而，这些用户的说法具有误导性。

<div>

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

</div>

我决定使用客户端 F3 屏幕数据进行一些分析，并为此开发了一个自定义的 Spigot [插件](https://github.com/LoneDev6/IAMEGBenchmark)。\
这些用户展示的 rx 值不准确，因为客户端计算这个值的方式有所不同。\
MEG v4 使用了包裹数据包，这允许客户端在处理一组数据包之前先等待一段时间。

包裹数据包的工作原理如下：

1. 服务器发送 `bundle start` 数据包
2. 服务器发送数据包（在这个案例中，MEG 发送显示实体的传送和显示实体的大小 + 旋转）
3. 服务器发送 `bundle end` 数据包

这意味着服务器总共发送了 4 个数据包，但客户端显示的 rx 值却是 1。\
这是因为游戏将包裹数据包视为一个单独的数据包，因此 F3 屏幕显示的值对于比较 v3 和 v4 或 ModelEngine 和 ItemsAdder 来说是不可靠的。

我使用了由 [EliteCreatures](https://a.devs.beer/elitecreatures-meg-comparison) 团队提供的模型进行了一些测试：一个有 35 个骨骼的船只模型。

{% tabs %}
{% tab title="MEG R4.0.2" %}
{% embed url="https://youtu.be/B1cxPPDNqVE?1" %}
{% endtab %}

{% tab title="MEG R3.1.9" %}
{% embed url="https://youtu.be/2zbLISIzRnA" %}
{% endtab %}
{% endtabs %}

### 结论

✅ IA 在实体静止不动且不在移动时发送的数据包较少（但实体仍在运行当前的动画）。\
❌ 目前，IA 在实体移动时发送的数据包 [更多](#user-content-fn-1)[^1]，相比于 MEG v3。\
❌ IA 与 MEG v3 相比缺少一些功能，但这些功能并不会在创建逼真的自定义实体时造成困难。请参见前面的对比表。

✅ MEG v3 对于移动实体的包使用量比 IA 低（减少了 30%）。\
❌ MEG v3 对于静止实体的包使用量比 IA 高（增加了 20%）。\
❌ MEG v3 中实体的行走/旋转看起来比较生硬，如 **之前的视频** 所示。

{% hint style="info" %}
在 ModelEngine v3 和 ItemsAdder 之间，数据包使用量的差异可以忽略不计。

ModelEngine v4 引入了显示实体的使用，这降低了数据包的使用量，因为这些实体的工作方式不同。

总之：你需要决定哪个插件最适合你的服务器项目。
{% endhint %}

[^1]: 原因尚不明确，可能与 ItemsAdder 处理自定义实体头/身体方向逻辑的方式有关，该方式接近原版 Minecraft。
