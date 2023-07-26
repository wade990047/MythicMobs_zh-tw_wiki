Mechanic: Set Game Mode
=======================

Sets the gamemode of the target player. Does nothing if the target is
not a player. Requires the `sync=true` attribute.

細項設定
----------

| Attribute | Aliases | Description   | Default Value |
|-----------|---------|---------------------------------------|---------------|
| mode  | m   | The gamemode to change the target to. | SURVIVAL  |

  

範例
--------

  Skills:
  - setgamemode{m=CREATIVE;sync=true} @PlayersInRadius{r=10} ~onSpawn
  - ...
