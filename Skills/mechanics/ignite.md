Mechanic: Ignite
================

Sets the targeted entity on fire.

細項設定
----------

| Attribute | Aliases  | Description   | Default |
|-----------|--------------|---------------------------------------|---------|
| ticks | t,d,duration | How many ticks the target should burn | 60  |

  

範例
--------

  Skills:
  - ignite{ticks=100} @trigger ~onAttack

Ignites the entity that the mob using this skill is attacking for 100
ticks (5 seconds).
