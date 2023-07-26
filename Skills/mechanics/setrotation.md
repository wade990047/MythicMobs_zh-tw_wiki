Mechanic: Set Rotation
======================

Changes the rotation of the target (only works on non-player entities).

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------------------|---------------|
| relative  | | If the change is relative to the target, boolean |   |
| yaw   | | The new yaw | 0 |
| pitch | | The new pitch   | 0 |

  

範例
--------

  Skills:
  - setrotation{relative=true;pitch=-45}
  - ...