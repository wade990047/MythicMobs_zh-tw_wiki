## 用途
Sets if the target raider should be a raider patrol leader or not


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
|  leader   | l, bool, b| Should the target raider be a leader|   true  |


## 範例
```yaml
  Skills:
  - setRaiderPatrolLeader{leader=true} @target
```


## 簡化寫法
- [x] setRaiderLeader