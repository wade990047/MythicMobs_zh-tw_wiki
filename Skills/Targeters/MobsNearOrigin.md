## 用途
將靠近技能觸發半徑內的指定怪物設為目標


## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 目標半徑範圍   | 5   |
| types | type, t   | 怪物類型，可以是一個列表 | |


## 範例
該技能結束時將點燃其周圍半徑範圍內指定類型的所有生物
```yaml
ExampleSkill:
  Skills:
  - projectile{...;
onEnd=[
  - ignite @MobsNearOrigin{r=10;types=IncredibleZombie,SpookyScarySkeleton}
]}
```