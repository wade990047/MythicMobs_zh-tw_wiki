用途
================

增加吸收效果的心
**適用於Minecraft版本 1.13+**

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-------------------|-------------|----------------|
| amount| a | 數量| 1  |
| maxabsorb | ma, ms | 最大數量| Amount's value |

  

範例
--------
```yml
  Skills:
  - shield{amount=50;maxShield=100} @self ~onSpawn
  - ...
```