用途
========================

更改目標位置的方塊類型

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------|---------------|
| material  | m   | 方塊類型 | [DIRT](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)  點擊查看其他詳細資訊|
| data  | md  | 方塊資料值   | 0 |

從版本 4018/4019 開始，可以設置方塊 mmoitems 自定義方塊。

下方範例，它將目標位置設置為 id 為 50 的 mmoitems 方塊。


範例
--------
```yml
SetBlockExample:
  Skills:
  - setblock{m=STONE;md=0} @selflocation

SetMMOItemsBlock:
  Skills:
  - setblock{m=mmoitems:50} @targetlocation

SetButton:
  Skills:
  - setblock{m=JUNGLE_BUTTON[facing=east,face=floor]} @targetlocation
```