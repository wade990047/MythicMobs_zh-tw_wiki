## 用途
Tests if the item entity is similar to an itemstack


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| item  | i, material, m, mm, mythicitem | The item to check against   | DIRT|


## 範例
```yaml
  TargetConditions:
  - entityitemissimilar{i=MyCustomItem} true
```