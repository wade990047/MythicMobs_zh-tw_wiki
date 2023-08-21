## 用途
將繼承目標周圍的隨機位置設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount    | a         | 點的數量             | 5       |
| radius    | r, maxradius, maxr | 最大半徑         | 5       |
| minradius | minr      | 最小半徑          | 0       |
| spacing   | s         | 每個目標的間隔               | 0       |


## 範例
```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @PIR{r=10}

ExampleSkill2:
  Skills:
  - effect:particles @RandomLocationsNearTargets{a=5;r=2}
```


## 簡化寫法
- [x] randomLocationsNearTarget
- [x] randomLocationsNearTargetEntities
- [x] randomLocationsNearTargetLocations
- [x] RLNT
- [x] RLNTE
- [x] RLNTL