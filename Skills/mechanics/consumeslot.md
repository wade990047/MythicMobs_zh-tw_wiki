用途
=================

從玩家物品欄的特定位置移除物品

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------------------------------------------------------------|---------|
| slot  | s   | 目標物品欄欄位. 允許欄位 0 到 35, 或是裝備欄位 | HAND| 
| amount| a   | 要移除的物品數量| 1   |

範例
--------

將移除玩家物品欄位編號為 0 的物品一個
```yml
Skills:
  - consumeslot{slot=0;amount=1} @NearestPlayer{r=10}
```
將移除玩家手上的物品一個
```yml
Skills:
  - consumeslot{slot=HAND;amount=1} @NearestPlayer{r=10}
```