## 用途
Checks the size of the target entity.  
Valid entities: `Slime`, `Magmacube`, `Phantom`


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| size  | s | The size to check for   | |


## 範例
```yaml
  TargetConditions:
  - size{s=>1} true
```


## 簡化寫法
- [x] mobSize