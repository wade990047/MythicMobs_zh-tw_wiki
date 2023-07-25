## 用途
Checks the target MythicMob's level


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| level | l | The level range to match| |


## 範例
```yaml
  Conditions:
  - level{l=10} true
```

```yaml
  Conditions:
  - level{l=>10} true
```

```yaml
  Conditions:
  - level{l=1to10} true
```

```yaml
  Conditions:
  - level{l=<10} true
```