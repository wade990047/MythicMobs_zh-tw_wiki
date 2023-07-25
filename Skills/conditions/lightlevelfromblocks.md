## 用途
Tests the light level originating from light-emitting blocks at the target location


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| level | l | The light level range to match  | 0   |


## 範例
```yaml
  Conditions:
  - lightlevelfromblocks{l=10} true
```

```yaml
  Conditions:
  - lightlevelfromblocks{l=>10} true
```

```yaml
  Conditions:
  - lightlevelfromblocks{l=1to10} true
```