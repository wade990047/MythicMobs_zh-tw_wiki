用途
================

移除目標生物(對玩家無效)

範例
--------

出生後 10 秒移除自己
```yml
  Skills:
  - remove{delay=200} @self ~onSpawn
```
當互動時移除自己
```yml
  Skills:
  - remove @self ~onInteract
```