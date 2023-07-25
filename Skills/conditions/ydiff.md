## 用途
Checks the difference in y value (height) between the target entity and the caster.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| difference| diff, d   | The y difference to check   | |


## 範例
```yaml
  TargetConditions:
  - yDiff{diff=>5} true
```