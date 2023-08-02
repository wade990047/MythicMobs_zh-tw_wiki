用途
======================

丟出飛濺藥水

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|--------------|----------------|-----------------------------------------------------------------|---------|
| type | t | 要使用的 [藥水類型](/databases/items/potions) | None|
| duration | d  | 持續時間(單位:ticks)| 100 |
| level| l  | 藥水效果等級 | 1   |
| velocity | v  | 丟藥水的速度  | 1   |
| hasParticles | p | 是否顯示粒子效果 (MM 4.6+) | true|
| hasIcon  | i  | 是否顯示藥水圖示 (MM 4.6+)  | true|

  

範例
--------
```yml
ThrownCripplingPotion:
  Skills:
  - shootpotion{t=SLOW;d=200;l=4;v=5} @target
```