## 用途
將繼承目標的區塊中的所有方塊設為目標

## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| noair | na| 是否不應將空氣作為目標  | true|
| onlyair   | oa| 是否只針對空氣 | false   |
| nearorigin| no| 目標選擇器是否應定位於起點   | false   |


## 範例
技能將針對技能樹觸發器所在區塊中的每個非空氣塊
```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @trigger

ExampleSkill2:
  Skills:
  - effect:particles @BlocksInChunk
```


## 簡化寫法
- [x] BIC