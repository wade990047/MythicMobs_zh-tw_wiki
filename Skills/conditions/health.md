## 用途
Matches the target's health


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| health| h, amount, a | The health range to check for| 0   |


## 範例

```yaml
Conditions:
- health{h=50} true
```

```yaml
# Below 50 health
Conditions:
- health{h=<50} true
```

```yaml
# Above 10 health
Conditions:
- health{h=>10} true
```


## 簡化寫法
- [x] hp