用途
-----
清除目標藥水效果

細項設定
-----
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|--------------|----------------|--------|---------|
| type  | | 要清除的效果類型  | |

不輸入則清除所有效果

範例
-----
```yml
Skills:
  - potionclear{type=FIRE_RESISTANCE} @target
  - potionclear{type=FIRE_RESISTANCE,SPEED} @self
  - potionclear{} @self
```