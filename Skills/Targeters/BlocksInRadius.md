## 用途
將繼承目標半徑內的所有方塊設為目標


## 細項設定 
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 目標半徑範圍   | 2   |
| radiusy   | ry, yradius, yr |  y 的半徑 | radius  |
| shape | s | 選擇涵蓋方塊的形狀類型。可以是 `SPHERE`, `CUBE`| SPHERE  |
| noise | n | 目標的隨機性   | 0   |
| noair | na| 是否不應將空氣作為目標  | true|
| onlyair   | oa| 是否只針對空氣 | false   |
| nearorigin| no| 目標器選擇是否應定位在起點| false   |


## 範例

技能將瞄準技能樹觸發器周圍半徑 10 格內的每個非空氣塊

```yaml
ExampleSkill1:
  Skills:
  - skill{s=ExampleSkill2} @trigger

ExampleSkill2:
  Skills:
  - effect:particles @BlocksInRadius{r=10}
```


## 簡化寫法
- [x] BIR