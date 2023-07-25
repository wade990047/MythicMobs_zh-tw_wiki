## 用途
Gives experience levels to the targeted players


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The amount of levels to give| 0   |


## 範例
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - giveexperiencelevels{a=1} @trigger ~onDamaged
```


## 簡化寫法
- [x] giveexplevels