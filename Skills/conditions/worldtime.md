## 用途
Matches a range against the target location's world's time.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| time  | t | A range of time to check| 0   |


## 範例
```yaml
  Conditions:
  - worldtime{t=0to6000} true
```