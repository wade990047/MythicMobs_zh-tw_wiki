用途
===============

將目標實體向外丟(由原點出發)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----|----------------|----|
| velocity  | v   | 向外丟的水平力量 | 1 |
| velocityY | vy  | 向外丟的垂直力量 | 1 |

  

範例
--------
```yml
地面衝擊:
  Skills:
  - effect:explosion @Self
  - damage{amount=10} @PlayersInRadius{r=5}
  - throw{velocity=15;velocityY=5} @PlayersInRadius{r=5}
```
範例中的技能會先在技能施放者的位置顯示一個爆炸效果，同時對半徑5格內的所有玩家造成10點傷害(五顆心)，並且讓玩家有向外(離開技能施放者)的力飛去，藉此模擬爆炸後的擊退