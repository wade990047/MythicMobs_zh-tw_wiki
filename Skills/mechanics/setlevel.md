Mechanic: Set Level
===================

*Introduced in version 2.2.1*

Causes the casting mob to change it's level.

Possible operations for the action value are SET, ADD, SUBTRACT,
MULTIPLY, and DIVIDE.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------------|---------------|
| action| a   | Type of operation to perform   | SET   |
| level | l   | Amount of levels used in the operation | 1 |

  

範例
--------

This will set the mob level to 3 when it spawns
```yml
- setlevel{a=set;l=3} @self ~onSpawn
```

This will increase the mob level by 1 each time it kills a player
```yml
- setlevel{a=add;l=1} ~onKillPlayer
```