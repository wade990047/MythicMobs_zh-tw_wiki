用途
===============

變數技能組，可使用佔位符(Placeholder) 作為技能名稱
用法與 [技能組](skills/mechanics/skill) 一樣只是允許在技能中使用變量作為技能名稱

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|-----------------|---------|
| skill | s | 要執行的技能名稱，允許 [佔位符](Skills/Placeholders) |  |
| forcesync | sync  | 是否強制該技能與Minecraft同步執行 | false   |


範例
--------
```yml
ExampleSkill:
  Skills:
  - vskill{s=ExampleSkill_<random.1to3>} @self

ExampleSkill_1:
  Skills:
  - effect:particles{particle=reddust;color=#FF0000;amount=10}
ExampleSkill_2:
  Skills:
  - effect:particles{particle=reddust;color=#FFFFFF;amount=10}
ExampleSkill_3:
  Skills:
  - effect:particles{particle=reddust;color=#00FF00;amount=10}
```
在上方範例中`ExampleSkill` 技能組一旦觸發，將執行名稱由 `ExampleSkill_` 和隨機生成的 1 到 3 之間的數字組成的技能。

#

```yml
Example_StanceSkill:
  Skills:
  - vskill{s=ExampleMob_<caster.stance>_<random.1to2>} @self
```
在上方範例中，VariableSkill 用於快速創建一些基於姿態的技能，而無需使用任何姿態條件等

#

```yml
Example_VariablePlaceholder:
  Skills:
  - vskill{s=Fireball_<skill.var.fireballtype>} @self
```
在上方範例中，VariableSkill 將執行一個技能組，其名稱取決於之前設置技能範圍變量