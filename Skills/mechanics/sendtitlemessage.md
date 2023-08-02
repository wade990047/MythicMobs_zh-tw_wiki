Mechanic: Send Title
====================

Displays a "title" and/or "subtitle" message to all targeted players.
Does nothing if the target is not a player.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------------------------|---------------|
| title | t | The title string to send. Must be in double-quotes.| NONE  |
| subtitle  | st  | The subtitle string to send. Must be in double-quotes. | NONE  |
| duration  | d   | How long the title will display (in ticks) | 1 |
| fadeIn| fi  | The fade-in time for the title (in ticks)  | 1 |
| fadeOut   | fo  | The fade-out time for the title (in ticks) | 1 |

  

範例
--------

  Skills:
  - sendtitle{title="Beware!";subtitle="A dangerous spell is being cast!";d=20} @PlayersInRadius{r=10}
  - ...
