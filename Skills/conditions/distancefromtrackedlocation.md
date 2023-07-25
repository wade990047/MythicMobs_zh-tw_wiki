## 用途
Checks if the distance between the entity and the tracked location is within the specified values


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| distance  | d | The values to check for. Can be a range.| |


## 範例
```yml
Conditions:
  - DistanceFromTrackedLocation{d=5} true
```
```yml
Conditions:
  - DistanceFromTrackedLocation{d=2to10} true
```

## 簡化寫法
- [x] distanceFromTL