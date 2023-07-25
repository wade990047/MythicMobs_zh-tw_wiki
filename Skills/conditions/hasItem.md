## 用途
Tests if the target player or an item container has exactly the given number of the given material.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| item  | i, material, m | The item to check for  | DIRT|
| amount| a | The amount to check for | >0  |


## 範例

```yaml
  Conditions:
  - hasitem{i=stick;amount=>1} true
```
```yaml
  Conditions:
  - hasitem{i=my_custom_item;amount=<10} true
```
```yaml
  Conditions:
  - hasitem{i=mmoitems.SWORD.CUTLASS;amount=1to10} true
```