## 用途
Checks the food saturation amount of the target


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a, food, f, saturation, s | Range of amount of food saturation to check for  | 0   |


## 範例
```yaml
  TargetConditions:
  - FoodSaturation{a=<1} true
```

## 簡化寫法
- [x] hungerSaturation