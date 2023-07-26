Mechanic: VariableAdd
=====================

Adds an amount to a [variable](/skills/variables) on the specified
scope. Only works with numeric variable types.

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|------------------------------------|---------------|
| var   | name, key | The scope and name of the varibale | None |
| amount| a   | The amount to add | 1 |

  

範例
--------

  Skills:
  - variableadd{var=skill.testVar;amount=1} ~onInteract
  - ...