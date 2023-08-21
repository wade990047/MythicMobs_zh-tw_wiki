用途
========================

目標或位置射出火焰彈

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|---------------|-----------|--------------------------------------------------------------------------------|---------------|
| yield | y | 爆炸威力| 1 |
| velocity  | v | 速度 | 1 |
| incendiary| i | 火焰彈是否會殘留火焰  | false |
| fireTicks | ft| 火焰存留時間 | 0 |
| smallfireball | small,sml | 是否替換成烈焰使者的火球 | false |
| playsound | ps| 是否播放聲音 | false |
| type  | t | 火球類型:SMALL/LARGE/DRAGON 新增於 MM v4.11 版 | SMALL |

  

範例
--------
```yml
FireballBarrage:
  Skills:
  - shootfireball{y=1;v=4} @target
  - delay 10
  - shootfireball{y=1;v=4} @target
  - delay 10
  - shootfireball{y=1;v=4} @target
```