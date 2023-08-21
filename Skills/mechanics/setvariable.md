用途
=====================

新增與設置一個 [變量](/skills/variables)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|------------------|---------------|
| variable  | n, var | 變量名稱 可以透過 **scope.** 來補足儲存位置的值  |   |
| value | val | 變量的值，值必須符合 **變量類型** 否則此技能將會出現錯誤，如果值含有空隔必須使用雙引號(")包住，值可以是任何已存在的佔位符，也可以是來自PlaceholderAPI中的佔位符 |   |
| scope | s   | 設置變量的 [變量儲存位置](/skills/variables#變量儲存位置)| SKILL |
| type  | t | 設置變量的 [變量類型](/skills/variables#變量類型)，若要使用文字務必要選擇 STRING| INTEGER |
| save  | | 是否在重新讀取、重新啟動和斷線時保存變量，**不適用儲存在技能樹的變量。**| false |
| duration  | d | 變量會存在多久(單位: ticks)。**不適用儲存在技能樹的變量。**| Infinite |

  
範例
----

在範例中，目標玩家在10分鐘內只會聽到來自附近的熊咆哮聲一次。
```yml
BearMob:
  Skills:
  - skill{s=BearGrowl} @PlayersInRadius{r=40} ~onTimer:60
```
```yml
BearGrowl:
  TargetConditions:
  - variableEquals{var=target.heardbear;value="yes"} cancel
  Skills:
  - message{m="&7You hear a growling noise..."}
  - setvariable{var=target.heardbear;value="yes";type=STRING;duration=6000}
```
---
在範例中，額外的技能:`IgnitionDamage`

只有在變量:`do_ignite`被設置為`yes`時觸發。
```yml
Strike:
  Skills:
  - setvariable{var=skill.do_ignite;type=STRING;value="yes"} 0.5
  - damage{amount=20}
  - skill{s=IgnitionDamage}

IgnitionDamage:
  Conditions:
  - varEquals{var=skill.do_ignite;value="yes"}
  Skills:
  - ignite{ticks=20}
```
---
在範例中，一個來自 MMOItems 的佔位符資料被儲存在 INTEGER 的變數類型中
```yml
PlaceholderDamage:
  Skills:
  - setvariable{var=caster.new_skill_damage;value="%mmoitems_stat_skill_damage%";type=INTEGER} @self
  - damage{a="100 * <caster.var.new_skill_damage>"} @PIR{r=5}
```
當然其他類型的佔位符也可以
```yml
VariableSend:
  Skills:
  - setvariable{var=caster.VariableA;value="%mmoitems_stat_skill_damage%";type=INTEGER} @self
  - setvariable{var=caster.VariableB;value="<caster.var.VariableA> * 2";type=INTEGER} @self
  - setvariable{var=caster.VariableC;value="<caster.var.VariableA> + <caster.var.VariableB>";type=INTEGER} @self
```