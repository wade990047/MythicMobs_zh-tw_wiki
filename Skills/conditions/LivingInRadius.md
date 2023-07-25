## 用途
Matches a range to how many living entities are in the given radius


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The amount to check for | 1   |
| radius| r | The radius of the search| 5   |


## 範例
```yaml
  Conditions:
  - livinginradius{a=<5;r=10} true
```