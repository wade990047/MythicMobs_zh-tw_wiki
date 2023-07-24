## 用途
將伺服器上的所有玩家設為目標

## 範例
```yaml
PlayerCount_ServerWide:
  Skills:
  - setvariable{var=skill.count;val=<skill.targets>} @PlayersOnServer{targetself=true}
  - message{m="There are <skill.var.count> entities loaded in the current world"} @self
```


## 簡化寫法
- [x] server
- [x] everyone