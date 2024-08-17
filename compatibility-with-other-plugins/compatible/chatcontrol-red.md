# ChatControl-Red

[点击下载](https://www.mc-market.org/resources/18217/)

ItemsAdder 表情符号兼容性：  
更多信息请访问：[https://github.com/kangarko/ChatControl-Red/issues/853#issuecomment-818497610](https://github.com/kangarko/ChatControl-Red/issues/853#issuecomment-818497610)

## 在聊天中添加自定义频道前缀

如果你想为你的频道创建一个图形化的前缀，并在聊天中显示，你可以按照以下教程操作。

![展示ARCADE频道前缀的示例](../../.gitbook/assets/image\_\(94\).png)

你只需在格式配置中设置这个（例如在ChatControl Red的`format/arcade.yml`文件中）：

```yaml
  prefix:
    Message: ':arcade:'
```

显然，你需要使用你自己的[font_image](../../plugin-usage/adding-content/font-images/)名称，而不是`arcade`，这是一个示例。

## 文字效果

通常情况下，ItemsAdder 的文字效果无法与 ChatControl Red 一起使用。  
但是，如果你将以下内容添加到 ChatControl Red 的 `rules` 文件夹中，它们将能够正常工作。（我将其放在 `global.rs` 文件中）。

```
match <r\s([^>]+)>
require perm ia.user.text_effect.use.r
strip colors false
then replace #FFFFFE$1&r
    
match <w\s([^>]+)>
require perm ia.user.text_effect.use.w
strip colors false
then replace #FFFFFD$1&r
    
match <j\s([^>]+)>
require perm ia.user.text_effect.use.j
strip colors false
then replace #FFFFFB$1&r
    
match <rw\s([^>]+)>
require perm ia.user.text_effect.use.rw
strip colors false
then replace #FFFFFC$1&r
    
match <rj\s([^>]+)>
require perm ia.user.text_effect.use.rj
strip colors false
then replace #FFFEFE$1&r
```
