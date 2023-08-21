用途
===============

使附近的其他生物一起攻擊目標

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------------|---------|----------------------------------------------------------------------------------------------------|---------------|
| types   | type, t | 生物類型，可以是一隻或列表 | NONE  |
| radius  | r   | 受影響的怪物半徑| 10|
| vradius | vr  | 平面半徑  | radius|
| hradius | hr  | 垂直半徑 | radius|
| overwritetarget | ot  | 是否重置已被指定的目標 | true  |

  

範例
--------

呼叫半徑 30 格內，所有怪物類型為 "Guard" 跟 "Knight" 的生物，攻擊觸發這個技能的實體
```yml
CallForHelp:
  Skills:
  - message{m="<mob.name><&co> Guards! Help me!"} @PlayersInRadius{r=30}
  - rally{types=Guard,Knight;radius=30;ot=false} @Trigger
```