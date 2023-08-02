用途
=================

改變目標實體的名稱(不適用於玩家)

範例
--------
```yml
Skills:
  - setname{name=newmobname} @self ~onDamaged 1
```
當受到傷害時將名稱改為 "newmobname"

```yml
MySkeleton:
  Type: Skeleton
  Display: 'Skeleton <caster.hp>/<caster.mhp><&heart>'
  Skills:
  - setname{name=<caster.name>;delay=2} @self ~onDamaged
  - setname{name=<caster.name>;delay=2} @self ~onTimer:10 ?incombat{}
```
將生物的名稱設置為其"Display:" 設定中的名稱(當受到傷害時) 以及在戰鬥中每 10 ticks 一次。

這是如何讓生物更新其名稱中的占位符的範例。在範例中，這樣做是為了更新 <caster.hp> 佔位符。
