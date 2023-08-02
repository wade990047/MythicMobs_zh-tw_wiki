Mechanic: SetGlobalScore
========================

為 變更計分板數值 of the fake player \_\_GLOBAL\_\_.
This is a notarget skill and cannot affect any other players' score.
Works exactly like the ModifyGlobalScore-mechanic, but is only capeable
of performing the **set**-action.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------------------------------------------------------------------------------------------------------|---------|
| objective | obj, o  | 記分板名稱，若不存在則自動創建 | |
| value | v   | 要使用的數值   | |

  
範例
----

- setglobalscore
{
o=someobjective;
v=2
} ~onAttack