## 用途
給予目標玩家經驗等級


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | 要給予的等級數量| 0   |


## 範例
```yml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - giveexperiencelevels{a=1} @trigger ~onDamaged
```


## 簡化寫法
- [x] giveexplevels