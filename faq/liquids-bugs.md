# 💧 液体Bugs

{% hint style="warning" %}
这些都是 Minecraft 的 bug，我无法修复。\
这就是游戏的工作方式。\
请不要报告这些问题。
{% endhint %}

### 自定义液体颜色与水混合，反之亦然

自定义液体有时不会完全着色，一些部分仍然保留了原版水的颜色。\
这是游戏工作方式的限制。我无法修复这个问题。

<details>

<summary>技术原因</summary>

Minecraft 将一个区块的生物群系存储在 int\[1024] 中。16x16x256=65536，这比 1024 要多得多。这意味着它以某种形式的块（具体大小不清楚）进行存储，因此更改特定的方块是不可能的。颜色在生物群系之间也会渐变，因此更改小的“块”总是看起来很奇怪，方块不会有完整的颜色。

来源：[https://www.spigotmc.org/threads/how-to-create-custom-biomes.512105/page-2#post-4243330](https://www.spigotmc.org/threads/how-to-create-custom-biomes.512105/page-2#post-4243330)

</details>

![](<../.gitbook/assets/image\_(14) (1) (2) (3) (3) (4) (4) (5) (7) (8) (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (13) (1) (1) (1) (11).png>)

### 我完全看不到液体颜色，即使将其放在不同的位置

你需要将生物群系混合设置为 `5x5` 或更低。

#### 不好

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

#### 好

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

## 液体在彼此之上显示相同的颜色

只有在你的客户端是 1.18.1 或更高版本时你才能做到这一点。\
旧版客户端无法正确显示这些颜色，这是游戏的限制。

{% hint style="warning" %}
如果你在自定义液体的顶部或底部放置普通水（或自然生成的水），你会发现它会呈现自定义液体的颜色。

**这是 Minecraft 的 bug，我无法修复。**
{% endhint %}

#### 不好 - 1.17.1 及以下版本

<figure><img src="../.gitbook/assets/water_bug_1.png" alt=""><figcaption></figcaption></figure>

#### 好 - 1.18.1 及以上版本

<figure><img src="../.gitbook/assets/water_bug_2.png" alt=""><figcaption></figcaption></figure>

## 液体不像水一样扩散！

{% hint style="success" %}
这是为了避免延迟和故障而按预期工作的。\
使用多个液体桶来放置更大的液体区域。
{% endhint %}

<figure><img src="../.gitbook/assets/water_bug_3.png" alt=""><figcaption></figcaption></figure>
