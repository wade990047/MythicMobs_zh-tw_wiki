## 用途
將施法者世界半徑內最近的指定類型結構設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| type      | t         | 結構類型     | STRONGHOLD |
| radius    | r         | 目標半徑範圍       | 5000    |
| unexplored | u        | 結構是否應該要是尚未被探索的                          | false   |


## 範例
```yaml
StrongholdFinder:
  Cooldown: 10
  Skills:
  - projectile{hp=false;se=false;sb=false;v=5;d=100;onTick=[ effect:particles ]} @NearestStructure{r=1000}
```