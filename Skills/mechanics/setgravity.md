Mechanic: Set Gravity
=====================

Sets whether gravity affects the target entity.

Attributes
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|-------------------------------------------------|---------------|
| gravity   | g   | Sets whether the entity uses gravity (boolean). | true  |

  

Examples
--------

  Skills:
  - setgravity{g=false} @self ~onSpawn
  - setusegravity{g=false} @self ~onSpawn
  - ...