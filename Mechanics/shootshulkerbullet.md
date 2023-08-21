用途
================================

設出界伏蚌的子彈，並給擊中的生物漂浮效果

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------------------|---------------|
| interval  | i   | 每多少 ticks 更新一次 | 4 |
| onTick| oT  | ticks 計算時要執行的技能  | NONE  |
| onHit | oH  | 擊中後要執行的技能 | NONE |
| onEnd | oE  | 結束後要執行的技能   | NONE  |


範例
--------

```yml
TestingShootShulkerBullet:
  Skills:
  - ShootShulkerBullet{oT=TSSB_oT;oH=TSSB_oH;oE=TSSB_oE;i=1} @target
  
TSSB_oT:
  Skills:
  - particles{particle=reddust;color=#ffffff;size=0.66;a=2;hs=0;vs=0;s=0;y=0} @origin
TSSB_oH:
  Skills:
  - damage{a=5}
TSSB_oE:
  Skills:
  - particlesphere{particle=reddust;color=#ffffff;size=0.66;a=30;r=1;hs=0;vs=0;s=0;y=0} @origin
```