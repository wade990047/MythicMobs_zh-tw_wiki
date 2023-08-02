## 用途
移除玩家手上的物品


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | 要移除的數量| 1   |


## 範例
```yml
ExampleSkill:
  Skills:
  - consumeHeldItem{amount=1} @trigger
```


## 簡化寫法
- [x] consumeHeldItem
- [x] takeHeldItem