## 用途
將繼承目標和施法生物之間一條線上的所有實體設為目標


## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 直線上每個點之間的距離以及實體將作為目標的每個點周圍的半徑 | 1   |
| fromorigin| fo| 這條線是否應該從技能的起點開始繪製 | false   |


## 範例
```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @Forward{f=10}

ExampleSkill2:
  Skills:
  - ignite @LivingInLine{r=0.5}
```


## 簡化寫法
- [x] entitiesInLine
- [x] livingEntitiesInLine
- [x] LEIL
- [x] EIL