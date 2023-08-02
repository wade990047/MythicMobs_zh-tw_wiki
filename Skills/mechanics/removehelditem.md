## 用途
Removes the given amount from the target player's held item. 


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The amount to remove| 1   |


## 範例
```yml
ExampleSkill:
  Skills:
  - consumeHeldItem{amount=1} @trigger
```


## 簡化寫法
- [x] consumeHeldItem
- [x] takeHeldItem