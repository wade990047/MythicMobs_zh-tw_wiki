## 用途
將生物和繼承目標之間的位置設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius    | r         | 直線上每個點之間的距離                          | 1       |
| fromorigin| fo        | 這條線是否應該從技能的起點開始繪製         | false   |


## 範例
```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @Forward{f=10}

ExampleSkill2:
  Skills:
  - effect:particles @Line{r=0.5}
```