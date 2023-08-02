Mechanic: Set Gravity
=====================

Sets whether gravity affects the target entity.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-------------------------------------------------|---------------|
| gravity   | g   | Sets whether the entity uses gravity (boolean). | true  |

  

範例
--------

  Skills:
  - setgravity{g=false} @self ~onSpawn
  - setusegravity{g=false} @self ~onSpawn
  - ...