用途
===================

給予目標指定物品/掉落集合

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-------------|---------|-------------------|---------------|
| item| i   | 物品 (可使用[自定義物品](https://git.lumine.io/mythiccraft/MythicMobs/-/wikis/Items/Items) 和 [掉落集合](https://git.lumine.io/mythiccraft/MythicMobs/-/wikis/drops/Drops#drop-tables)) |   |
| fakeLooting | fl  | 是否播放拾取動畫 | false |

------------

**筆記:**

當玩家背包滿時這項技能將沒有任何效用  

範例
--------
```yml
Skills:
- giveitem{i=diamond_sword} @PIR{r=20} ~onSpawn
- ...
```