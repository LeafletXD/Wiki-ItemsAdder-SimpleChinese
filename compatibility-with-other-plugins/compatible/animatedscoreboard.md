# AnimatedScoreboard

## [点击下载](https://www.spigotmc.org/resources/animatedscoreboard.20848/)

{% hint style="warning" %}
请在寻求帮助之前参考插件页面的教程。我并不是该插件的开发者，因此此信息可能会随着时间的推移而变得过时。
{% endhint %}

## 记分板中的字体图像

如果安装了 **PlaceholderAPI**，你可以在记分板中使用 [字符图像](../../plugin-usage/adding-content/font-images/)（表情符号和符号）。

### 示例

`%img_smile%` 将显示如下：

![](../../.gitbook/assets/animatedscoreboard\_1.png)

## 隐藏记分板背景

使用 ItemsAdder，你可以隐藏记分板的背景，只需使用这个小技巧。

（适用于支持 PlaceholderAPI 的所有记分板插件）

{% tabs %}
{% tab title="之前" %}
​

<figure><img src="https://files.gitbook.com/v0/b/gitbook-legacy-files/o/assets%2F-M28TcKgSDvuFN510qye%2F-MhOfUmIRJYMhFZM2AQy%2F-MhOgJ6DpHjDR8dc9NYc%2Fimmagine.png?alt=media&#x26;token=1a5efcc3-27a5-49b4-80c9-c98ebcb197d2" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="之后" %}
​\\

<figure><img src="https://files.gitbook.com/v0/b/gitbook-legacy-files/o/assets%2F-M28TcKgSDvuFN510qye%2F-MhOfUmIRJYMhFZM2AQy%2F-MhOg9VxfKvE2ZGZ3QE6%2Fimmagine.png?alt=media&#x26;token=c4ee2fd0-2aa9-46e2-a8dd-0025dcc64f7e" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}
### 如何隐藏背景

你只需要在记分板配置的<mark style="color:yellow;">**每一行**</mark>前面添加 `%img_offset_-500%`，<mark style="color:yellow;">即使是在空行上也要添加!</mark>

{% hint style="danger" %}
#### 警告！

与 **AnimatedScoreboard** 的特殊属性不兼容，例如这些和类似的：

`<health full=&4 half=&c empty=&f update=5>❤</health>`

`<repeat times=10>|</repeat>`

`<stay ticks=100>&lAnimated Scoreboard</stay>`

<mark style="color:red;">请不要向我寻求支持</mark>，我无法修复这个问题，我不是 **AnimatedScoreboard** 的作者。

如果你想使用 `<stay>`，你需要把 `%img_offset_-500%` 放在第一个 `>` 之后。\
示例：

`<stay ticks=100>%img_offset_-500%&lAnimated Scoreboard</stay>`
{% endhint %}

<details>

<summary>&#x3C;--- 点击这里获取示例 YML 配置文件</summary>

{% code title="defaultscoreboard.yml" %}
```yaml
display:
    title:
      text:
      - "%img_offset_-500%&lA"
      - "%img_offset_-500%&lAn"
      - "%img_offset_-500%&lAni"
      - "%img_offset_-500%&lAnim"
      - "%img_offset_-500%&lAnima"
      - "%img_offset_-500%&lAnimat"
      - "%img_offset_-500%&lAnimate"
      - "%img_offset_-500%&lAnimated"
      - "%img_offset_-500%&lAnimated "
      - "%img_offset_-500%&lAnimated S"
      - "%img_offset_-500%&lAnimated Sc" 
      - "%img_offset_-500%&lAnimated Sco"
      - "%img_offset_-500%&lAnimated Scor"
      - "%img_offset_-500%&lAnimated Score"
      - "%img_offset_-500%&lAnimated Scoreb"
      - "%img_offset_-500%&lAnimated Scorebo"
      - "%img_offset_-500%&lAnimated Scoreboa"
      - "%img_offset_-500%&lAnimated Scoreboar"
      - "%img_offset_-500%&lAnimated Scoreboard"
      - "%img_offset_-500%&c&lAnimated Scoreboard"     
      - "%img_offset_-500%&lAnimated Scoreboard"
      - "%img_offset_-500%&c&lAnimated Scoreboard"
      - "%img_offset_-500%&lAnimated Scoreboard"
      - "%img_offset_-500%&c&lAnimated Scoreboard"
      - "<stay ticks=100>%img_offset_-500%&lAnimated Scoreboard</stay>"
      random: false
      interval: 2
    line-1:
      text:
      - "%img_offset_-500%"
      random: false
      interval: 200
      score: 99   
    line-2:
      text:
      - "%img_offset_-500%&a&lWelcome %player_name%"
      - "%img_offset_-500%&b&lWelcome %player_name%"
      - "%img_offset_-500%&c&lWelcome %player_name%"   
      random: false
      interval: 5
      score: 98
    line-3:
      text:
      - "%img_offset_-500%"
      random: false
      interval: 20
      score: 97
    line-4:
      text:
      - "%img_offset_-500%&aYour gamemode:"
      - "%img_offset_-500%&aYour location:"
      - "%img_offset_-500%&aYour world:"    
      random: false
      interval: 60
      score: 96
    line-5:
      text:
      - "%img_offset_-500% &b%player_gamemode%"
      random: false
      interval: 60
      score: 95
    line-6:
      text:
      - "%img_offset_-500% &bX:%player_x% Y:%player_y% Z:%player_z%"
      random: false
      interval: 1
      score: 95
    line-7:
      text:
      - "%img_offset_-500% &b%player_world%"    
      random: false
      interval: 60
      score: 95
    line-8:
      text:
      - "%img_offset_-500%"
      random: false
      interval: 200
      score: 95
    line-9:
      text:
      - "%img_offset_-500%&1Random Rotation"
      - "%img_offset_-500%&2Random Rotation"
      - "%img_offset_-500%&3Random Rotation"
      - "%img_offset_-500%&4Random Rotation"
      - "%img_offset_-500%&5Random Rotation"
      - "%img_offset_-500%&6Random Rotation"
      - "%img_offset_-500%&7Random Rotation"
      - "%img_offset_-500%&8Random Rotation"
      - "%img_offset_-500%&9Random Rotation"
      - "%img_offset_-500%&aRandom Rotation"
      - "%img_offset_-500%&bRandom Rotation"
      - "%img_offset_-500%&cRandom Rotation"
      - "%img_offset_-500%&dRandom Rotation"
      - "%img_offset_-500%&eRandom Rotation"
      - "%img_offset_-500%&kRandom Rotation" 
      - "%img_offset_-500%&lRandom Rotation" 
      - "%img_offset_-500%&mRandom Rotation" 
      - "%img_offset_-500%&nRandom Rotation"
      - "%img_offset_-500%&oRandom Rotation"
      - "%img_offset_-500%&rRandom Rotation"       
      random: true
      interval: 1
      score: 94
    line-10:
      text:
      - "%img_offset_-500%"       
      random: true
      interval: 1
      score: 93
```
{% endcode %}

</details>
