用途
=================

擊中目標後造成傷害並恢復自身生命值

細項設定
----------

| 設定項| 簡化寫法 | 用途   | 預設值 |
|------------------|---------|---------------------------------------|---------|
| damage   | d,dmg   | 要造成的傷害量  | 1|
| heal | h   | 造成傷害後要恢復的血量 | None|
| preventknockback | pkb, pk | 是否取消傷害擊退   | false   |
| preventimmunity  | pi  | 是否取消傷害無敵   | false   |
| ignorearmor  | i,ia| 是否無視盔甲 | false   |

*"preventknockback" 和 "preventimmunity" 新增於 MM v2.3*  

範例
--------

對半徑20格內的所有殭屍造成 1000 點傷害，每隻被傷害的殭屍將為施法者恢復 20 點血量

  Skills:
  - consume{d=1000;h=20} @MobsInRadius{type=ZOMBIE;r=20}