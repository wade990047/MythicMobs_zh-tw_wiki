## 用途
將繼承目標的實體位置設為目標

## 範例
```yaml
ExampleSkill1:
  Skills:
  - skills{s=ExampleSkill2} @EIR{r=10}

ExampleSkill2:
  Skills:
  - lightning @LocationsOfTargets
```


## 簡化寫法
- [x] locationOfTarget
- [x] LOT