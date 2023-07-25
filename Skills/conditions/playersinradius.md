## 用途
Checks how many players are in a radius.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | The given range value to check  | >0  |
| radius| range, r  | The given radius to check   | 32  |


## 範例
```yaml
  Conditions:
  - playersinradius{a=>3;r=16}
```


## 簡化寫法
- [x] pir
- [x] playerInRadius