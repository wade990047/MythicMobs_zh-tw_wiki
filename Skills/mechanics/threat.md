Mechanic: Threat
================

Modifies the mob's threat value towards the target. Requires the mob
have Threat Tables enabled in order to have any effect.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-----------------------------------------------------------|---------|
| amount| a   | The amount of threat to give the target. Can be negative. | 1   |
| mode  | m   | Add / Remove / Multiply / Divide / Set / Reset / Forcetop | Add |

Set/reset/forcetop modes do not require the “amount=” field  

範例
--------

This example will set the nearest player's threat level to a very high
amount.

Fixate:
  Skills:
  - threat{amount=10000} @NearestPlayer ~onSpawn
