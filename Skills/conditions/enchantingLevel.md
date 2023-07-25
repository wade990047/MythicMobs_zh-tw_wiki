## 用途
Checks the target player's experience level


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| level | l | Range of amount of experience level to check for | 0   |


## 範例
```yaml
  TargetConditions:
  - EnchantingLevel{l=<10} true
```