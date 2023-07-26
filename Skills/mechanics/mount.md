Mechanic: Mount
===============

Causes the casting mob to summon a specified MythicMob and mount it.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------|---------------|
| type  | t   | The type of MythicMob to summon. |   |

  

Special Notes
-------------

The MythicMob defines in type must be a valid MythicMob type (and is
case-sensitive). If an invalid type is specified the skill may throw an
error.

範例
--------

This example would summon a Mythic Mob of the type "UndeadMount" and
make the caster mount it.

  CallSkeletalHorse:
Skills:
- mount{type=UndeadMount}
