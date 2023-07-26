用途
===============

貼上 FAWE 的選取建築 (插件:Fast Async World Edit): [FAWE](https://www.spigotmc.org/resources/fast-async-worldedit.13932/)

您必須在 MythicMob 資料夾中創建一個 `Schematics` 資料夾，並將你要使用的藍圖放入該資料夾中。<br>
如果在 MM 的 `Schematics` 資料夾中找不到技能中定義的藍圖，則請檢查 FAWE 和 WE 是否存在

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------|---------------|
| schematic |  s   | 結構名稱 |   |
| pasteAir | air,a   | 是否也要貼上空氣 | true |
| xOffset | x,xo  | 貼上結構的目標左右偏移值   | 0 |
| yOffset | y,yo  | 貼上結構的目標上下偏移值  | 0 |
| zOffset | z,zo  | 貼上結構的目標前後偏移值   | 0 |
| chestDropTable | chests,cdt  | 儲物箱裡的物品要用MM的哪個掉落集合   | "" |
| trappedchestDropTable | trapchests,tcdt  | 陷阱儲物箱裡的物品要用MM的哪個掉落集合   | "" |
| blocksPerTick  || 每ticks要放置多少方塊  |   |
| pasteID   | pid, id | 執行貼上的動作id. 可以用在 [還原貼上] 的技能裡 |   |
  

範例
--------
```yaml
  - fawePaste{schematic=deserttempleiron.schem;y=6;air=true;chestDropTable=IronDropTable} @origin
```


  [還原貼上]: /Skills/mechanics/undopaste