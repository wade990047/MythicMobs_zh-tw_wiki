用途
==============

光環系列技能對實體起到狀態效果的作用，並且可以在其持續時間內觸發其他技能。

光環允許建立自訂追蹤其狀態效果(即增益和減益)持續時間，也可用於其他技能和條件。

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|---------------------|---------|------------------|---------------|
| auraName| | 自訂名稱 | None  |
| onStartSkill | os | 光環執行時首先觸發的技能 | None  |
| onTickSkill  | ot | 每觸發一次 **Tick** 計算時所執行的技能 | None  |
| onEndSkill   | oe | 光環結束後所執行的技能  | None  |
| ShowBarTimer | bt | 設置後，光環將在施法期間顯示一個施法條
| Charges | c | 設置後，當使用次數達到零時，光環就會消失。可由其他技能修改。 | 0 |
| Duration| d | 光環最大持續時間(單位: ticks)  | 200   |
| Interval| i   | 每隔多少 **Tick** 執行一次 `onTickSkill`| 1 |
| maxStacks | ms | 最多對同一個目標施加幾次光環 (v4.6.0+)   | None  |
| refreshDuration | rd | 如果實體被再次施加相同的光環，則使光環的持續時間刷新(v4.6.0+) | true |
| mergeSameCaster | msc | 將一個實體施加於另一個實體的所有相同光環合併為一個光環(防止生物能夠在同一實體上多次疊加光環)(v4.6.0+)   | false |
| mergeAll| ma | 將任意和所有實體施加於另一個實體的所有相同光環合併為一個光環（防止多個生物能夠在同一實體上多次堆疊光環） (v4.6.0+) | false |
| overwriteSameCaster | | 啟用後，停止同一施法者對目標施加的相同光環，並用新光環取代 | false |
| overwriteAll | |啟用後，停止應用在目標上的所有相同光環，並用新光環取代| false |
| CancelOnGiveDamage  | cogd| 實體造成傷害時結束光環 | false |
| CancelOnTakeDamage  | cotd| 實體受到傷害時結束光環 | false |
| CancelOnDeath   | cod | 實體自身死亡時結束光環 | true  |
| CancelOnTeleport| cot | 實體進行傳送時結束光環 | false |
| CancelOnChangeWorld | cocw| 實體變更世界時結束光環 | false |
| CancelOnSkillUse| cosu| 實體使用技能時結束光環| false |
| CancelOnQuit| coq | 玩家退出遊戲時結束光環  | true  |
| DoEndSkillOnTerminate | desot | 當技能被 [auraremove](skills/mechanics/auraremove) 移除時是否執行 `onEndSkill` | true |

  
===== 特殊設定 (v4.6.0+)=====  
**onAttack** 光環類型有下列額外設定項:

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|------------------|---------------|------------------------------------------------------------|---------------|
| onHit| oH| 當實體造成攻擊時所執行的技能  | NONE |
| cancelEvent  | cE| 是否取消觸發光環的事件 | false |
| damageAdd| a| 增加傷害量(負值為減少) | 0 |
| damageSub   | s| 減少傷害量(負值為增加) | 0 |
| damageMultiplier | m | 造成傷害的額外倍率 | 1   |

The **onDamaged** aura type has the following options:

-   All options available to Auras

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|------------------|---------------|------------------------------------------------------------|---------------|
| onHit| oH| Skill to execute if the target is damaged  | NONE|
| cancelEvent  | cE| Whether or not to cancel the event that triggered the aura | false |
| damageSub   | sub, s| An optional static decrease (or increase if negative) to the original hit's damage | 0 |
| damageMultiplier | multiplier, m | An optional multiplier on the original hit's damage | 1 |

(See example below for usage)

範例
--------

  Skills:
  - Aura{auraName=Retributing_Light;onTick=RetributingLightDamage;interval=10;duration=240} @self

Gives the target (Which in this case is the entity itself) the
Retributing_Light aura that lasts 12 seconds. Every 10 ticks (or half a
second) it will fire the RetributingLightDamage skill.

 Skills:
  - onDamaged{auraName=fire_shield;onHit=FireShield;duration=200;charges=5;multiplier=0.5} @self

In this example, the caster's next 5 hits taken in 10 seconds would
trigger the FireShield skill targeting whatever hit them and also deal
50% damage. However, if FireShield's conditions failed, it would deal
regular damage as the multiplier would not trigger either.

  Skills:
  - onAttack{auraName=fiery_strikes;onHit=FireStrike;duration=200;charges=5;multiplier=2} @self

In this example, the caster's next 5 physical hits within 10 seconds
would trigger the FireStrike skill targeting whatever was hit and also
deal 200% damage. However, if FireStrike's conditions failed, it would
deal regular damage as the multiplier would not trigger either.