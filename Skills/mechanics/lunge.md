Mechanic: Lunge
===============

Applies forward directional velocity to the target.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------|---------------|
| velocity  | v   | The horizontal velocity at which the entity is moved forward. | 1 |
| velocityY | vy  | The vertical velocity at which the entity is moved forward.   | 1 |
| oldmath   | old, o  | If the lunge mechanic should use the old math formula | false |

  

範例
--------

- lunge{velocity=15;velocityY=5} @Self