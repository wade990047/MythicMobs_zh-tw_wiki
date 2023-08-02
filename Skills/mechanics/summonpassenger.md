## 用途
Summons a mob to mount the caster. Will knock the current rider off if there is one.


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| passenger | p. rider, r, type, t | The type of the mob to set as the passenger   | |

  
## 範例
```yml
  Skills:
  - summonPassenger{type=MyZombie}
```
Will summon the mob "MyZombie" to ride the caster of the mechanic.


## 簡化寫法
- [x] passenger
- [x] summonRider
- [x] rider