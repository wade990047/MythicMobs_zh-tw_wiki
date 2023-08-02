## 用途
設置目標顯示的轉換同型實體


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| action| a | 要執行的動作. 可以是 `SET`, `ADD`, `MULTIPLY`, `DIVIDE` | SET |
| transformationtype | transformation, type, tt | 要轉換的型態. 可以是 `TRANSLATION`, `SCALE`, `RIGHT_ROTATION`, `LEFT_ROTATION`| TRANSLATION |
| value | val   | 轉換參數 | 0,0,0   |


## 範例
```yml
ExampleDisplayEntity:
  Type: block_display
  Skills:
  - displaytransformation{action=set;transformation=translation;value=0,0,1} @self ~onDamaged
```


## 簡化寫法
- [x] settransformation
- [x] transformation