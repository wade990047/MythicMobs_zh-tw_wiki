Mechanic: Set Game Mode
=======================

Sets the gamemode of the target player. Does nothing if the target is
not a player. Requires the `sync=true` attribute.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------|---------------|
| mode  | m   | The gamemode to change the target to. | SURVIVAL  |

  

範例
--------

  Skills:
  - setgamemode{m=CREATIVE;sync=true} @PlayersInRadius{r=10} ~onSpawn
  - ...
