用途
================
對目標怪物發送信號

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------|---------------|
| signal| s   | 要發送的信號 | ping  |

  

範例
--------

在受傷時讓 "Master" 發出信號 "ATTACK"，給半徑10格內的 "Minion"

當 "Minion" 接收到信號 "ATTACK" 對最近的玩家執行技能 "ShootAttacker"

怪物檔案:
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
技能檔案:
```yml
ShootAttacker:
  Skills:
  - shoot{t=arrow}
```