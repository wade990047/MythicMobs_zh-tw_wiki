## 用途
Checks a scoreboard value of the target entity.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| objective | obj, o| The objective   | |
| entry | ent, e| The entry  | |
| value | val, v| The value to match  | |


## 範例
```yaml
  Conditions:
  - score{o=PlayerKills;e=Akim91;v=10} true
```