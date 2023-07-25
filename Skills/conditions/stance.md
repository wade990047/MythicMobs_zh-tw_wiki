## 用途
Checks the stance of the target mob.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| stance| s | The stance to match | DEFAULT |
| strict| str   | Whether to match exactly| false   |


## 範例
```yaml
  Conditions:
  - stance{s=CombatStance;str=true} true
```