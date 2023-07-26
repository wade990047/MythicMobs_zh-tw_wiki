Mechanic: undoPaste
===============
Undoes a previous paste done via the [fawePaste] mechanic, based on its id or on the schematic used

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------|---------------|
| schematic |  s   | The schematic that needs to be undone. Only necessary if no id can be provided | |
| pasteID   | pid, id  | The id of the paste that needs to be undone  |   |

## 範例
```yaml
ExampleMob:
  Skills:

  # With ID
  - fawePaste{s=cgym.schem;id=abc} @self ~onSpawn
  - undoPaste{id=abc} @self ~onDamaged

  # Without ID
  - fawePaste{s=lab.schem} @self ~onSpawn
  - undoPaste{id=lab.schem} @self ~onDamaged
```

[fawePaste]: /Skills/mechanics/fawepaste/