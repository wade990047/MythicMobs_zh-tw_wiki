Mechanic: Prison
================

Encases the target entity inside a temporary prison of blocks. The
created blocks will disappear automatically after the specified
duration.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------------------------------|---------------|
| material  | m   | The Material (block type) the prison is made out of. | ICE   |
| duration  | d   | How long (in ticks) the prison will last | 100   |
| breakable | b   | (true/false) Whether or not the prison blocks can be broken. | false |

  

範例
--------

This skill creates a iron block prison around the target of the casting
mob, for 200 ticks (10 seconds), and the prison can be mined.

IronPrison:
  Skills:
  - prison{material=IRON_BLOCK;duration=200;breakable=true} @target
