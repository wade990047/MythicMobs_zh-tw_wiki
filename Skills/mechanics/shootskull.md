Mechanic: Shoot Skull
=====================

Shoots a wither skull from the mob towards the target entity or
location.

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------------|---------------|
| yield | y   | The yield (power) of the skull's explosion. | 1 |
| playsound | ps  | Whether or not to play the skull launching sound when it is created | false |

  

範例
--------

This example would shoot a barrage of 3 fast-moving Wither Skulls at the
target.

SkullBarrage:
  Skills:
  - shootskull{y=1;v=4} @target
  - delay 10
  - shootskull{y=1;v=4} @target
  - delay 10
  - shootskull{y=1;v=4} @target
