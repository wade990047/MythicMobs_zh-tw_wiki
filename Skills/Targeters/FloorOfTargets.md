## 用途
將繼承目標的實體下方的方塊設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| tries     | t, max, m | 目標選擇器改變目標資料的最大次數 | 3 |


## 範例
該機制會將半徑 10 格內每個玩家下方的方塊遮蓋成冰
```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @PIR{r=10}

ExampleSkill2:
  Skills:
  - blockmask{r=1;m=ICE} @FloorOfTargets
```


## 簡化寫法
- [x] floorsOfTarget
- [x] FOT