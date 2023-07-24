## 用途
將當前世界的所有玩家設為目標

## 範例
```yaml
PlayerCount:
  Skills:
  - setvariable{var=skill.count;val=<skill.targets>} @PlayersInWorld{targetself=true}
  - message{m="There are <skill.var.count> entities loaded in the current world"} @self
```


## 簡化寫法
- [x] World