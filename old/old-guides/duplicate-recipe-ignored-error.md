# “Duplicate recipe ignored” 错误

如果您遇到类似的错误，请更新您的 Paper 或 Spigot 到 **最新版本**。即使是 1.14.4 版本，也不意味着它已经是最新的，您需要下载其 **最新版本**。

```text
Server thread/ERROR Error occurred while enabling ItemsAdder v1.1.27 (Is it up to date?)
java.lang.IllegalStateException: Duplicate recipe ignored with ID itemsadder:philosopher_stone
at net.minecraft.server.v1_14_R1.CraftingManager.addRecipe(CraftingManager.java:72) ~[minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.craftbukkit.v1_14_R1.inventory.CraftShapedRecipe.addToCraftingManager(CraftShapedRecipe.java:59) ~[minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.craftbukkit.v1_14_R1.CraftServer.addRecipe(CraftServer.java:1102) ~[minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.Bukkit.addRecipe(Bukkit.java:639) ~[minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at dev.lone.itemsadder.d.e.a.c.a(Unknown Source) ~[?:?]
at dev.lone.itemsadder.d.d.b.b(Unknown Source) ~[?:?]
at dev.lone.itemsadder.d.d.b.aY(Unknown Source) ~[?:?]
at dev.lone.itemsadder.d.d.b.c(Unknown Source) ~[?:?]
at dev.lone.itemsadder.d.a.reload(Unknown Source) ~[?:?]
at dev.lone.itemsadder.d.a.(Unknown Source) ~[?:?]
at dev.lone.itemsadder.Main.bh(Unknown Source) ~[?:?]
at dev.lone.itemsadder.Main.onEnable(Unknown Source) ~[?:?]
at org.bukkit.plugin.java.JavaPlugin.setEnabled(JavaPlugin.java:263) ~[minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.plugin.java.JavaPluginLoader.enablePlugin(JavaPluginLoader.java:352) [minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.plugin.SimplePluginManager.enablePlugin(SimplePluginManager.java:417) [minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.craftbukkit.v1_14_R1.CraftServer.enablePlugin(CraftServer.java:461) [minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at org.bukkit.craftbukkit.v1_14_R1.CraftServer.enablePlugins(CraftServer.java:375) [minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at net.minecraft.server.v1_14_R1.MinecraftServer.a(MinecraftServer.java:449) [minecraft_server.jar:git-Spigot-9de398a-9c887d4]
at net.minecraft.server.v1_14_R1.DedicatedServer.init(DedicatedServer.java:258) [minecraft_server.jar:git-Spigot-9de398a-9c887d4]
```

