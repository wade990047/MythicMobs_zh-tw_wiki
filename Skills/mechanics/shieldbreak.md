Mechanic: Shield Break
--------------------------

Breaks the target player's shield block if they are blocking. Only works when targeting players.

細項設定
----------

| Attribute | Aliases| Description | Default Value |
|-----------|------------|----------------------------------------------------------------------------------------------------------------|---------------|
| duration  | d  | The duration in ticks that the shield will be disabled for after the block is broken | 100  |

  

範例
--------

If the player is blocking, this would break the block and put the shield on cooldown for 200 ticks (or 10 seconds.)

Skills:
- shieldbreak{duration=200} @target