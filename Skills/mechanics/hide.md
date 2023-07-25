Mechanic: Hide
===================

Hides the caster from the targeted players for a set duration.
A duration of `0` will permanently hide the caster.
Only works for MC 1.18+.

Attributes
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|--------------------|---------------|
| duration  | d   | The given duration | 0 |

Added in MM 4.13

------------

Examples
--------
```yml
  DUMMY:
Type: ZOMBIE
Skills:
- hide{d=100} @Server ~onInteract
```
```yml
  CUSTOM_ITEM:
Id: STICK
Skills:
- hide{d=100} @Server ~onUse #User is now invisible from all online players, no armor is shown
```