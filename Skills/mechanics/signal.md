Mechanic: Signal
================

*Added in version 2.2.1*

Sends a signal to the specified targeter. Won't do anything when
targeted at players. The signal can be composed of any string. The
mob(s) that receives the signal can only act upon it if it has a
dedicated "~onSignal" trigger in its skill arsenal (see examples).

The signal can either be matched by comparing directly behind the
trigger (~onSignal:*ping*) or by the new
[lastsignal-condition](http://www.mythicmobs.net/manual/doku.php/conditions/start).

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|--------------------|---------------|
| signal| s   | The signal to send | ping  |

  

範例
--------

This example would make the "Master" mob signal it's minions a radius of
20 blocks to shoot an arrow the nearest players, relative to the minions
positions, upon being damaged.

Mobfile:
```yml
Master:
  Type: zombie
  Skills:
  - summon{m=Minion} @self ~onSpawn
  - signal{s=ATTACK} @MobsInRadius{r=10;t=Minion} ~onDamaged
Minion:
  Type: baby_zombie
  Skills:
  - skill{s=ShootAttacker} @NearestPlayer ~onSignal:ATTACK
```
Skillfile:
```yml
ShootAttacker:
  Skills:
  - shoot{t=arrow}
```