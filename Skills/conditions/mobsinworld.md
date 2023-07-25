## 用途
Matches a range to how many mobs are in the target world


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The number range to match   | 0   |


## 範例
```yaml
  Conditions:
  - mobsinworld{a=20to50} true
```

```yaml
  Conditions:
  - mobsinworld{a=<50} true
```