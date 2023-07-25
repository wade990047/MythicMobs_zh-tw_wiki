## 用途
This condition checks if the target player has a permission. 


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| permission| p | The permission to check for.| |


## 範例

```yaml
  Conditions:
  - haspermission{p=permission.node.here} true
```
```yaml
  TargetConditions:
  - haspermission{p=permission.node.here} true
```
```yaml
  TriggerConditions:
  - haspermission{p=permission.node.here} true
```


## 簡化寫法
- [x] permission