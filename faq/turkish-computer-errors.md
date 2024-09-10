# 🇹🇷 🇹🇷 土耳其 计算机报错

如果你遇到如下随机错误：

```log
java.lang.IllegalArgumentException: Symbol does not appear in the shape
```

可以通过在 Java 启动参数中添加以下内容来修复此问题：`-Duser.language=en`

例如，如果你正在使用 [Aikar's flags](https://docs.papermc.io/paper/aikars-flags)：

`java -Xms10G -Xmx10G -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1`` `<mark style="color:green;">`-Duser.language=en`</mark>` ``-Dusing.aikars.flags=https://mcflags.emc.gs -Daikars.new.flags=true -jar paper.jar --nogui`

（翻译者：这好像是土耳其翻译者为英文Wiki上传了什么文件，不过我还是翻译了，或许对你有用）
