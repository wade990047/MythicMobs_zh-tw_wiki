## 用途
[變量](/Skills/Variables) 是否等於指定值

## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|-------------------|---------|
| variable  | n, var | 變量名稱，可以通過 **scope.** 來補足設定項| |
| value| val, v | 變量的值，值必須符合 **變量類型** 否則此技能將會出現錯誤，如果值含有空隔必須使用雙引號(")包住，值可以是任何已存在的佔位符，也可以是來自PlaceholderAPI中的佔位符| |
| scope| s| 變量的 [變量儲存位置](/skills/variables#變量儲存位置) | |


## 範例

在範例中，目標玩家在10分鐘內只會聽到來自附近的熊咆哮聲一次。
```yml
BearMob:
  Skills:
  - skill:BearGrowl @PlayersInRadius{r=40} ~onTimer:60
```
```yml
BearGrowl:
  TargetConditions:
  - variableEquals{var=target.heardbear;value="yes"} cancel
  Skills:
  - message{m="&7You hear a growling noise..."}
  - setvariable{var=target.heardbear;value="yes";duration=6000}
```
---
在範例中，`PoisonStormDamage`只會在全域(global)變量`poison_storm`被設置為`yes`時才會執行
```yml
PoisonStormDamage:
  Conditions:
  - varEquals{var=global.poison_storm;value="yes"}
  Skills:
  - potion{type=POISON;duration=100}
  - damage{amount=1;ignorearmor=true}
```