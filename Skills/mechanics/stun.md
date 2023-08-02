用途
==============

使目標實體暈眩

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|---------------------|---------|--------------------------------------------------------------------------------------------------------------|---------------|
| duration| d   | 持續時間(單位:ticks) |   |
| stopai  | ai  | 是否將ai暫時停止| false |
| gravity | g   | 是否暫時移除重力 (Minecraft 1.9+) | false |
| facing  | face, f | 是否無法轉頭| false |
| noknockback | nokb, kb | 是否不能擊退| false |
| CancelOnGiveDamage  | cogd| 是否造成傷害時解除暈眩| false |
| CancelOnTakeDamage  | cotd| 是否受到傷害時解除暈眩  | false |
| CancelOnDeath   | cod | 是否死亡時解除暈眩 | true  |
| CancelOnTeleport| cot | 是否傳送時解除暈眩 | false |
| CancelOnChangeWorld | cocw| 是否切換世界時解除暈眩 | false |
| CancelOnSkillUse| cosu| 是否使用技能時解除暈眩  | false |
| CancelOnQuit| coq | 是否登出時解除暈眩  | true  |

  

特別筆記
-------------
這項技能有可能造成 Spigot踢出玩家 (玩家移動錯誤!)

範例
--------

暈眩目標 3 秒，並且不能轉頭
```yml
Freeze:
  Skills:
  - stun{d=60;f=true} @target
```