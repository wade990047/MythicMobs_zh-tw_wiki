Mechanic: Drop Item
===================

在目標位置掉落指定物品或[掉落集合](/databases/drops/overview).

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------------------------------------------------------------|---------------|
| items | i   | 要掉落的物品，可以是獨立物品、物品集合、用,分割的物品列 | NONE  |

範例
--------

掉落指定物品列的範例.
```yaml
  Skills:
  - dropitem{i=diamond_sword,diamond} @self ~onDeath
  - ...
```
掉落指定物品集合的範例
```yaml
  Skills:
  - dropitem{i=SkeletonKingDrops} @self ~onSpawn
  - ...
```