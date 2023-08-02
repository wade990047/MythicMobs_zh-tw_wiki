用途
====================

對目標玩家送出標題與副標題訊息

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------------------------|---------------|
| title | t | 大標題訊息，需使用(")| NONE  |
| subtitle  | st  | 副標題訊息，需使用(") | NONE  |
| duration  | d   | 顯示持續時間(單位:ticks)| 1 |
| fadeIn| fi  | 淡入時間(單位:ticks)| 1 |
| fadeOut   | fo  | 淡出時間(單位:ticks) | 1 |

  

範例
--------
```yml
  Skills:
  - sendtitle{title="Beware!";subtitle="A dangerous spell is being cast!";d=20} @PlayersInRadius{r=10}
  - ...
```