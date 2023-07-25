## 用途
Checks the experience points that the target player has.


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| level | l | The experience points to check for. Accepts ranges.  | 0   |


## 範例
```yaml
  TargetConditions:
  - enchantingExperience{l=>100} true
```

## 簡化寫法
- [x] enchantingExp
- [x] enchantExperience
- [x] enchantExp