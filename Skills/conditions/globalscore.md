## 用途
Checks a global scoreboard value (the value associated with the fake player __GLOBAL__)


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| objective | obj, o| The objective   | |
| value | val, v| The value to match  | |


## 範例
```yaml
  Conditions:
  - globalscore{o=KillCount;value=5} true
```


## 簡化寫法
- [x] scoreglobal