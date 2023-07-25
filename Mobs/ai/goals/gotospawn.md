Goal: goToSpawnLocation
--------------

*Aliases*: goToSpawn

Makes the mob travel to its original spawn location.

### 細項設定

| Attribute  | Aliases  | Description| Default |
|----------------|----------|------------------------------------|:-------:|
| speed  | s| Movement speed modifier|1|
| minRange | min | How far the mob needs to be from its spawn location to consider itself "at the location". The mob will walk towards its spawn location until it is this close to it. |   2|
| maxRange | max | The maximum range the mob can be from its spawn location. If the mob is further than this amount from its spawn location, it will activate the goal and walk towards the spawn location until it reaches the minimum range. |   16|
| dropTarget | dt | Whether or not the mob should drop its current target when this goal activates. |   true|


### 範例

This zombie will try to melee attack its target until it is more than 20 blocks from its spawn location, then will turn around and walk back to where it spawned.
```yaml
ExampleMob:
  Type: ZOMBIE
  AIGoalSelectors:
- clear
- goToSpawn{speed=1;max=20;min=4}
- meleeattack
```