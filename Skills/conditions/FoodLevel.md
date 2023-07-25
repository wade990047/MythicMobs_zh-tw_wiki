## 用途
Checks the food amount of the target


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a, food, f| Range of amount of food to check for| 0   |


## 範例
```yaml
  TargetConditions:
  - FoodLevel{a=<10} true
```


## 簡化寫法
- [x] hunger
- [x] food
- [x] hungerlevel