用途
================

給予目標藥水效果, 在 [這裡](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/potion/PotionEffectType.html) 
可以看到所有可用藥水效果

過高的藥水等級可能會有反效果

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|--------------|----------------|-------------------------------------------------------------------------------------------|---------|
| type | t | 要套用的 [藥水效果](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/potion/PotionEffectType.html) | |
| duration | d  | 效果持續時間(單位:ticks) | 100 |
| level| l  | 藥水效果等級，實際等級為設定值+1 | 1   |
| force|| 是否強制覆蓋已有的藥水效果 (MM v4.0 以上版本)  | false   |
| hasParticles | p | 是否顯示藥水粒子 (MM v4.6 以上版本)  | true|
| hasIcon  | i  | 是否顯示藥水圖示 (MM v4.6 以上版本)   | true|

範例
--------

對目標造成 10 秒 緩速V 並附帶 10 點傷害
```yml
Cripple:
  Skills:
  - potion{type=SLOW;duration=200;level=4}
  - damage{amount=10}
```