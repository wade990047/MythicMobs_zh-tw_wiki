## 用途
Tests the light level at the target location


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| level | l | The level range to match| 0   |


## 範例
```yaml
  Conditions:
  - lightlevel{l=10} true
```

```yaml
  Conditions:
  - lightlevel{l=>10} true
```

```yaml
  Conditions:
  - lightlevel{l=1to10} true
```