## 用途
Targets random locations near the caster


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount    | a         | The amount of points             | 5       |
| radius    | r, maxradius, maxr | The radius in which target points will be generated         | 5       |
| minradius | minr      | The minimum radius in which target points will be generated          | 0       |
| spacing   | s         | The minimum amount of space between selected targets                 | 0       |


## 範例
```yaml
ExampleSkill:
  Skills:
  - effect:particles @RandomLocationsNearCaster{a=5;r=2}
```


## 簡化寫法
- [x] randomLocations
- [x] RLNC