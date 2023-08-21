## 用途
變量數值是否在範圍內

## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|-|---------|
| variable  | name, n, var, key, k | 要檢查的變量| |
| value | val, v, range, r | 範圍  | | 


## 範例

```yml
  Conditions:
  - variableInRange{var=caster.Cooldown;value=<0.01} cancel
  Skills:
  - setvariable{var=caster.Cooldown;type=float;value="10"}
  - message{m="&7Cooldown over!"}
```