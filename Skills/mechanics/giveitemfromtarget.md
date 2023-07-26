Mechanic: Give Item From Target
===============================

Gives the caster an item while playing the pickup-item animation from the target entity or location when fakelooting is set to true.

Gives the caster an item from the target entity or location when fakelooting is set to false.

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-------------|---------|-------------------|---------------|
| item| i   | The item material (supports for mythicmobs item) | None |
| amount  | a   | The amount given  | 1 |
| fakeLooting | | plays the pickup-item animation from the target | false |

------------

This mechanic was added in 4.12 MM

範例
--------

Skills:
- giveitem{i=diamond_sword;a=1} @PIR{r=20} ~onSpawn
- ...