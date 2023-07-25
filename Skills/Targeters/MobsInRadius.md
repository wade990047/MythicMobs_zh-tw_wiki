## 用途
將半徑內的所有指定怪物設為目標


## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 目標半徑範圍   | 5   |
| types | type, t   | 怪物類型，可以是一個列表 | |


## 範例
```yaml
ExampleSkill:
  Skills:
  - ignite @MobsInRadius{r=10;types=IncredibleZombie,SpookyScarySkeleton}
```


## 簡化寫法
- [x] MIR