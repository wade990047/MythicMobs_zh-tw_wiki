## 用途
Matches the number of players online


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The number of players to check for. Can be a range   | 0   |


## 範例
```yaml
  Conditions:
  - playersOnline{amount=>5}
```