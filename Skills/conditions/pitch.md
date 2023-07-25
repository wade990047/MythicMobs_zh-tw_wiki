## 用途
Checks if the pitch of the target entity is within a range


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| pitch | p | The number range to match   | |



## 範例
```yaml
  Conditions:
  - pitch{p=-45to45} true
```

```yaml
  Conditions:
  - pitch{p=>45} true
```