## 用途
Checks the MythicMob type of the target mob


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| type  | types, t  | A list of MythicMob types to match  | |


## 範例
```yaml
  Conditions:
  - mythicmobtype{t=CoolZombie,IceZombie,SnowZombie} true
```

```yaml
  TargetConditions:
  - mythicmobtype{t=HotZombie,LavaZombie,FireZombie} true
```


## 簡化寫法
- [x] mmType