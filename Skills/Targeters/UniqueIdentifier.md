## 用途
將指定UUID的生物設為目標，支援 Placeholder


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| uuid      | u         | 實體的uuid           | 0       |


## 範例
下面的生物會記住他生成後第一個擊中他的實體的 uuid，並且會每 10 秒點燃他
```yaml
VengefulMob:
  Type: ZOMBIE
  Skills:
  - setvariable{var=caster.targetedentity;type=STRING;val=<trigger.uuid>} @self ~onDamaged =100% ?~isLiving
  - ignite @UniqueIdentifier{uuid=<caster.var.targetedentity>} ~onTimer:200 ?variableisset{var=caster.targetedentity}
```


## 簡化寫法
- [x] uuid