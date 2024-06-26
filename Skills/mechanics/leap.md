用途
==============

讓施法者向前衝刺.

Leap 類似於投射物的軌跡，生物會以拋物線形式移動，

力量足夠大就會降落在目標前，不夠則盡可能的像目標靠近

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-------------------------------------------|---------------|
| velocity  | v   | 向目標的力量  | 100   |
| noise | | 生物實際抵達地點的偏差值 | 1 |

  

特別筆記
-------------

由於該技能的運作方式，使用非常高的力量值（通常超過 100 效果會最好）。

此技能的計算方式與大多數技能不同。

範例
--------

該技能會讓生物跳向高處的目標，然後猛烈撞擊地面並引起爆炸

```yml
CrushingLeap:
  Cooldown: 10
  Skills:
  - leap{velocity=200} @target
  - delay 20
  - jump{velocity=-100}
  - effect:explosion @self
  - damage{amount=20} @EntitiesInRadius{r=5}
```