## 用途
將目標的位置設為目標. 對於 [目標篩選器](/Skills/Metaskills#targets-filtering) 十分實用並且配合 [目標設定項](/Skills/Targeters#targeter-options).
## 範例
```yaml
ExampleSkill1:
  Skills:
  - skills{s=ExampleSkill2} @PlayerLocationsInRadius{r=10}

ExampleSkill2:
  Skills:
  - lightning @TargetedLocation{}
```


## 簡化寫法
- [x] targetedLocations
- [x] targetedLoc