# 事件

### ItemsAdderLoadDataEvent

```java
package dev.lone.itemsadder.api.Events;
public class ItemsAdderLoadDataEvent extends Event
```

当 ItemsAdder 正确加载所有内容时会触发此事件（同样适用于 `/iareload`）。\
监听此事件，以确保所有物品、图像等内容已可供您的插件使用。

### ResourcePackSendEvent - [文档](https://github.com/LoneDev6/API-ItemsAdder/blob/master/src/main/java/dev/lone/itemsadder/api/Events/ResourcePackSendEvent.java)

当服务器向客户端发送资源包时触发的事件。\
该事件包括**URL**、**哈希值**，并且包含有关是否为**ItemsAdder 资源包**或**其他插件资源包**的信息。

## 其他事件

{% embed url="https://github.com/LoneDev6/API-ItemsAdder/tree/master/src/main/java/dev/lone/itemsadder/api/Events" %}
