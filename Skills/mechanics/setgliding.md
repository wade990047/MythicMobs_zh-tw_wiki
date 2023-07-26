Mechanic: Set Gliding
=====================

Makes an elytra-equipped entity glide or stop gliding. This only works
on players or entities that have elytra equipped in the chestplate slot.
The targeted entity also has to be in the air at the time!

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------------------------------|---------------|
| gliding   | g   | If the entity is forced to glide or not. | true  |

  

Special Note
------------

In 1.10, the glide animation is bugged out for gliding mobs. This will
be fixed in 1.11.

範例
--------

This example will make the mob glide if it has elytra equipped and is in
the air at the time.

MakeMobGlide:
  Skills:
  - setgliding{g=true;} @self
