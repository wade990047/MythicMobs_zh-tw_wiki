## 用途
Sets the targeted display entity's transformations


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| action| a | The action to use. Can be `SET`, `ADD`, `MULTIPLY`, `DIVIDE` | SET |
| transformationtype | transformation, type, tt | The type of the transformation. Can be `TRANSLATION`, `SCALE`, `RIGHT_ROTATION`, `LEFT_ROTATION`| TRANSLATION |
| value | val   | The value of the transformation | 0,0,0   |


## 範例
```yaml
ExampleDisplayEntity:
  Type: block_display
  Skills:
  - displaytransformation{action=set;transformation=translation;value=0,0,1} @self ~onDamaged
```


## 簡化寫法
- [x] settransformation
- [x] transformation