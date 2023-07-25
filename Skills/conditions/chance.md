## 用途
Sets the probability of the metaskill being executed.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| chance| c | The floating value which denotes the chance. It can range between 0 and 1, with 0 being a 0% chance and 1 being a 100% chance |   0.5   |

## 範例
In this example, the metaskill will be executed only 30% of the times it has been triggered, on average.
```yaml
Conditions:
  - chance{chance=0.3} true
```

In this other example, the metaskill will be instead triggered 70% of the times it has been triggered
```yaml
Conditions:
  - chance{chance=0.3} false
```