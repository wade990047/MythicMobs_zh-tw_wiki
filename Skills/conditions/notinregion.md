## 用途
Checks if the target location is **not** within the given WorldGuard region


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| region| r, name, n| The region's name   | |


## 範例
```yaml
  Conditions:
  - notinregion{r=BossZone} true
```