## 用途
Whether the distance from the world's spawn point to the target is within the given range


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| distance  |   d   | The distance to match   | |


## 範例
```yaml
  Conditions:
  - distancefromspawn{d=<100} true
```
```yaml
  Conditions:
  - distancefromspawn{d=>50} true
```