用途
---------------------

沿著直線到達目標. **[付費版限定]**
 
細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|----------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| entityskill  |es| 當直線命中實體時執行的技能 |   |
| locationskill|ls| 當直線命中位置時執行的技能 |   |
| headshotskill|hs| 當直線命中頭部時執行的技能 |   |
| maxdistance  | md   | 直線的最大距離| 50|
| raywidth | rw | 直線的寬度  | 0.2   |  |
| ignorepassableblocks | ip| 忽略可通過方塊的碰撞(如:草、花...) | true  |
| fluidcollisionmode   | fcm   | [直線追踪過程中流體受到撞擊時的碰撞箱](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/FluidCollisionMode.html) | NEVER |
| accuracy | ac, a | 擊中擴散範圍 | 1 |
| verticalnoise| vn| 平面擴散範圍   | 0 |
| horizontalnoise  | hn| 垂直擴散範圍 | 0 |
| raytraceConditions   | rc|  直線的條件判斷式| NONE  |
| headshotmultiplier   | hsm | 命中頭部的力量倍率| 1 |

範例
--------

```yml
  - raytrace{
  entitySkill=[
- damage{amount=20}
  ];
  headshotSkill=[
- effect:particles{particle=reddust;color=#ff0000}
  ];
  locationSkill=[
- particles{p=flame;a=20;s=0.2;hS=0.1;vS=0.1}
  ];
  raytraceConditions=[
- samefaction false
  ]} @targetlocation ~onUse
```