## 用途
將繼承目標附近的所有玩家設為目標

## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 目標半徑範圍   | 5   |


## 範例
對生物目標半徑 2 格內的每個玩家造成傷害
```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @target

ExampleSkill2:
  Skills:
  - damage{a=10} @PlayersNearTargetLocations{r=2}
```


## 簡化寫法
- [x] playersNearTargetLocation
- [x] PNTL