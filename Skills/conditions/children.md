## 用途
Checks how many children the caster has.


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The amount of children to check for. Can accept ranged values.   | 1   |



## 範例
```yaml
  Conditions:
  - children{a=1} true
```
```yaml
  Conditions:
  - children{a=>2} true
```