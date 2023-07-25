## 用途
Checks if the given numeric variable is within a certain range.


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| variable  | name, n, var, key, k | Variable to match| |
| value | val, v, range, r | A number range to match  | | 


## 範例

```yaml
  Conditions:
  - variableInRange{var=caster.Cooldown;value=<0.01} cancel
  Skills:
  - setvariable{var=caster.Cooldown;type=float;value="10"}
  - message{m="&7Cooldown over!"}
```


## 簡化寫法
- [x] varinrange
- [x] varrange