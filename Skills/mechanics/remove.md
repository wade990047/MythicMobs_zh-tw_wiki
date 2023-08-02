Mechanic: Remove
================

Removes the targeted entity from existence. Does not work on players.

範例
--------

This mob would despawn 10 seconds after spawning:
```yml
  Skills:
  - remove{delay=200} @self ~onSpawn
```
This skill despawns the mob immediately when it is right clicked.
```yml
  Skills:
  - remove @self ~onInteract
```