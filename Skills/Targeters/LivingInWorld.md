## 用途
將世界內的所有實體設為目標

## 範例
```yaml
EntityCount:
  Skills:
  - setvariable{var=skill.count;val=<skill.targets>} @LivingInWorld
  - message{m="There are <skill.var.count> entities loaded in the current world"} @self
```


## 簡化寫法
- [x] EIW