## 用途
Checks how many mobs are in a given radius


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| types | type, t   | The types of mobs to check for  | |
| amount| a | The range of mobs to check for  | |
| radius| r | The radius to check | |


## 範例
```yaml
  Conditions:
  - mobsInRadius{types=NewZombie;amount=5to10;radius=15}
```