## 用途
Sets a cooldown on items of a specified material on the target player


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
|  material | mat, m| The material to set the cooldown to | ENDER_PEARL |
| duration  | d | The duration of the cooldown| 100 |


## 範例
```yml
  Skills:
  - setmaterialcooldown{m=CHORUS_FRUIT;d=150} @PIR{r=10}
```