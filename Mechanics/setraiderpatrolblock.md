## 用途
設置突襲者的巡邏位置


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| location  |block, l, b| 一個 [位置目標選擇器] | |  


## 範例
```yml
  Skills:
  - setRaiderPatrolBlock{l=@TrackedLocation} @self
```

## 簡化寫法
- [x] setRaiderBlock

[位置目標選擇器]: /Skills/Targeters#位置目標選擇器