用途
====================

對目標玩家送出成就框訊息

細項設定
----------

| Attribute | Aliases | Description   | Default Value  |
|-----------|---------|-------------------------------------------------------------------------------------|----------------|
| icon  | i   | 圖示  | diamond_sword |
| iconnbt   | nbt | 圖示的NBT資料  | NONE   |
| message   | msg,m   | 訊息，需使用(") | NONE   |
| frame | f   | 顯示的類型(必須是小寫)，設定項有: challenge, task, goal. | challenge  |

  

範例
--------
```yml
  Skills:
  - sendtoast{icon=DIAMOND; iconnbt={CustomModelData:1};message="Kill a boss!";frame=challenge} @PlayersInRadius{r=10}
  - ...
```
