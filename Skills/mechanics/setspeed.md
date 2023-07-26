Mechanic: Set Speed
===================

Causes the target to change its speed attribute

細項設定
----------

| Attributes | Description| Default Value |
|------------|-----------------------------------------|---------------|
| speed  | Speed of the entity | 1 |
| type   | Type of speed, can be WALKING or FLYING | WALKING   |

  

範例
--------

This will set the mob's walking speed to 2 when it spawns

- setspeed{speed=2;type=walking} ~onSpawn
