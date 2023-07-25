## 用途
Tests the type of the targeted entity item


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| material  | mat, m, type, types, t | A list of items to match   | |


## 範例
```yaml
  TargetConditions:
  - entityItemType{m=MyMythicItem,MyFantasticStick} true
```