## 用途
Checks if the number of inherited targets from the parent skilltree matches the given range.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | Range of how many targets to check for  | >0  |


## 範例
```yaml
  Conditions:
  - targets{a=>0} true
```

```yaml
  Conditions:
  - targets{a=0to5} true
```