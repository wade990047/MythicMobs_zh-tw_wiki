## 用途
Checks the yaw of the target entity against a range.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| yaw   | y | The yaw to check for| 0   |


## 範例
```yaml
  Conditions:
  - yaw{y=90to180} true
```

```yaml
  Conditions:
  - yaw{y=>0} true
```