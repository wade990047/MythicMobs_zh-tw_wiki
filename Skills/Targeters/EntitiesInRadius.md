## 用途
將半徑內的所有實體設為目標


## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | 目標半徑範圍   | 5   |
| livingonly| living, l | 目標是否應該只針對生物類實體 | true|


## 範例
```yaml
  Skills:
  - ignite @EIR{r=10}
```


## 簡化寫法
- [x] livingEntitiesInRadius  
- [x] livingInRadius  
- [x] allInRadius  
- [x] EIR