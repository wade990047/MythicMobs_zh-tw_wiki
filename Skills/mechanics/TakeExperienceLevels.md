## 用途
Takes experience levels to the targeted players


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The amount of levels to take| 0   |


## 範例
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - takeexperiencelevels{a=1} @trigger ~onDamaged
```


## 簡化寫法
- [x] takeexplevels