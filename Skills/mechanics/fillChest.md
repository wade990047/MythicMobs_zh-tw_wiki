用途
===================

將箱子填充指定物品或[掉落集合](Items/Drops#drop-tables)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------------------------------------------------------------|---------------|
| items | i   | 要填充的物品/物品列/掉落集合 | NONE  |
| shouldStack |   | 如果可堆疊的話，給予的物品是否堆疊 | |
| shouldempty | empty | 添加物品之前是否清空儲物箱| |

範例
--------

填充指定物品
```yml
  Skills:
  - fillchest{i=diamond_sword,diamond} @Location{x=#;y=#;z=#} ~onDeath
```
填充指定掉落集合
```yml
  Skills:
  - fillchest{i=SkeletonKingDrops} @Location{x=#;y=#;z=#} ~onSpawn
  ```