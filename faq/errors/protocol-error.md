# 协议错误

### NoClassDefFoundError

如果你遇到关于协议的错误，请使用最新的 ProtocolLib [https://www.spigotmc.org/resources/protocollib.1997/](https://www.spigotmc.org/resources/protocollib.1997/)

```
Error occurred while enabling ItemsAdder v1.1.16 (Is it up to date?)
java.lang.NoClassDefFoundError: com/comphenix/protocol/events/PacketListener
```

### 无法从 ID 获取实体 | Cannot retrieve entity from ID

要解决此问题，请使用最新的 ProtocolLib [http://ci.dmulloy2.net/job/ProtocolLib%20Gradle/lastStableBuild/artifact/build/libs/ProtocolLib.jar](http://ci.dmulloy2.net/job/ProtocolLib%20Gradle/lastStableBuild/artifact/build/libs/ProtocolLib.jar)​

```
[ItemsAdder] Unhandled exception occured in onPacketReceiving(PacketEvent) for ItemsAdder
java.lang.RuntimeException: Cannot retrieve entity from ID.
	at com.comphenix.protocol.wrappers.BukkitConverters$9.getSpecific(BukkitConverters.java:646) ~[?:?]
	at com.comphenix.protocol.wrappers.BukkitConverters$9.getSpecific(BukkitConverters.java:625) ~[?:?]
	at com.comphenix.protocol.reflect.StructureModifier.readInternal(StructureModifier.java:227) ~[?:?]
	at com.comphenix.protocol.reflect.StructureModifier.read(StructureModifier.java:195) ~[?:?]
	at dev.lone.itemsadder.Spigot.SpigotEntityFix$1.onPacketReceiving(Unknown Source) ~[?:?]
	at com.comphenix.protocol.injector.SortedPacketListenerList.invokeReceivingListener(SortedPacketListenerList.java:114) ~[?:?]
	at com.comphenix.protocol.injector.SortedPacketListenerList.invokePacketRecieving(SortedPacketListenerList.java:67) ~[?:?]
	at com.comphenix.protocol.injector.PacketFilterManager.handlePacket(PacketFilterManager.java:590) ~[?:?]
	at com.comphenix.protocol.injector.PacketFilterManager.invokePacketRecieving(PacketFilterManager.java:557) ~[?:?]
	at com.comphenix.protocol.injector.netty.ProtocolInjector.packetReceived(ProtocolInjector.java:352) ~[?:?]
	at com.comphenix.protocol.injector.netty.ProtocolInjector.onPacketReceiving(ProtocolInjector.java:317) ~[?:?]
​
```
