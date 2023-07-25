## 用途
Checks if the given skill is in cooldown for the target entity


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| skill | s | The metaskill to check  | |


## 範例
```yaml
  TargetConditions:
  - skillOnCooldown{skill=TestSkill}
```