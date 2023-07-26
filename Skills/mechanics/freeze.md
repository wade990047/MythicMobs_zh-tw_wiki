用途
================

對目標使用粉雪凍結效果並凍結指定的時間. 玩家的凍結效果上限為 140 ticks. (需求版本 1.17+)

細項設定
----------

| 設定項 | 簡化寫法 | 用途  | 預設值 |
|-----------|---------|-------------------------------|---------|
| ticks | t   | 被凍結的時間(單位:ticks) | 60  |

範例
--------
凍結使用施法者正在攻擊的實體 100 ticks (5秒).
```yaml
  Skills:
  - freeze{ticks=100} @trigger ~onAttack
```
由於遊戲處理凍結狀態的方式，上述範例可能不起作用。如果發生這種情況，可以執行以下技能處理
```yaml
#付費版
Freeze_CauseFreezeEffect_Inline:
  Skills:
  - aura{d=100;i=1;onTick=[  - freeze{ticks=280} - damage{a=1;cd=2;damagecause=FREEZE} ]} @self

#普通版
Freeze_CauseFreezeEffect_Normal:
  Skills:
  - aura{d=100;i=1;onTick=Freeze_CauseFreezeEffect_Normal_onTick} @self
Freeze_CauseFreezeEffect_Normal_onTick:
  Skills:
  - freeze{ticks=280}
  - damage{a=1;cd=2;damagecause=FREEZE}
```