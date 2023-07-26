Mechanic: GoTo
============================

Causes the mob to pathfind to a location.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|---------------|---------|-------------------------------------------------------------------------------|---------------|
| speedModifier | s   | The movement speed modifier  | 1 |
| spreadH   | sh  | Amount of horizontal spread it can be away from the target its moving towards | 0 |
| spreadV   | sv  | Amount of vertical spread it can be away from the target its moving towards   | 0 |

  

範例
--------
```yml
Skills:
  - goto{speedModifier=1;sh=5;sv=5} @owner
  - goto{speedModifier=1;sh=5;sv=5} @location{c=100,65,100}
```
