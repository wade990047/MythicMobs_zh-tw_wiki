## 用途
將繼承目標的實體設為目標. 對於 [目標篩選器](/Skills/Metaskills#targets-filtering) 非常實用，可以配合 [目標選擇器](/Skills/Targeters#targeter-options).
## 範例
```yaml
ExampleSkill1:
  Skills:
  - skills{s=ExampleSkill2} @PIR{r=10}

ExampleSkill2:
  Skills:
  - lightning @TargetedTarget{}
```


## 簡化寫法
- [x] targeted