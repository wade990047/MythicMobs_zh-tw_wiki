Mechanic: SetTargetScore
========================

*Added in version 2.3*

Modifies the a scoreboard-objective value of the specified targeter(s).
Works exactly like the ModifyTargetScore-mechanic, but is only capeable
of performing the **set**-action.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------------------------------------------------------------------------------------------------------|---------|
| objective | obj, o  | 記分板名稱，若不存在則自動創建 | |
| value | v   | 要使用的數值   | |

  
範例
----

This example will track how often and whom damaged
the casting mob in battle.

  Skills:
  - settargetscore
  {
  o=damagescore;
  value=1
  } @trigger ~onDamaged
