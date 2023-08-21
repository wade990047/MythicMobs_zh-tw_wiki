## 用途
將指定名稱的玩家設為目標，支援 Placeholder

## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| name      | n         | 玩家名稱           | CarsonJF|


## 範例
生物會記住他生成後第一個擊中它的玩家名字，並且之後會每 10 秒點燃他們
```yaml
VengefulMob:
  Type: ZOMBIE
  Skills:
  - setvariable{var=caster.targetedplayer;type=STRING;val=<trigger.name>} @self ~onDamaged =100% ?~isPlayer
  - ignite @PlayerByName{name=<caster.var.targetedplayer>} ~onTimer:200 ?variableisset{var=caster.targetedplayer}
```


## 簡化寫法
- [x] specificplayer