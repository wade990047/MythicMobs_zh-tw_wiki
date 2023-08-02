Mechanic: Teleport
==================

Teleports the caster to the targeted location/entity. The end point of the teleportation will be within an area whose size depends on the `spreadh` and `spreadv` attributes.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------------------------------------|---------------|
| spreadh   | sh  | The horizontal spread of the landing location. | 0 |
| spreadv   | sv  | The vertical spread of the landing location.   | 0 |

  

Special Notes
-------------

The skill will attempt to find a safe landing location within the spread
area, if possible, and should generally avoid putting the mob inside of
blocks.

範例
--------

This example would teleport the mob to within 5 blocks of the targeted
player, on the same vertical axis.

```yml
Warp:
  Skills:
  - teleport{spreadh=5;spreadv=0} @target
```