## 用途
Tests if the target has a scoreboard tag


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| tag   | t | The tag to check for| |


## 範例
```yaml
  Conditions:
  - hastag{t=KilledBoss1} true
```

```yaml
  TargetConditions:
  - hastag{t=PuzzleRoom1Solved} true
```


## 簡化寫法
- [x] hasScoreboardTag