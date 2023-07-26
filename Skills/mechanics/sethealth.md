Mechanic: Set Health
====================

Sets the health of the target entity.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-----------------------------|---------------|
| amount| a   | Amount of health to set to. | 1.0   |

  

範例
--------

This example will set the players' health to 6 (3 hearts) when they
right-click the mob.

  Skills:
  - sethealth{a=6} @trigger ~onInteract
  - ...
