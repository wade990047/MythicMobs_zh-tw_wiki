用途
===================

設置目標生物的姿態(只適用Mythicmobs)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-------------------------------|---------------|
| stance| s   | 姿態名稱 | default   |

範例
--------

將施法者的姿態設為 "bowphase"
```yml
StanceChangeSkill:
  Skills:
  - setstance{stance=bowphase} @self
```
技能只會在姿態為 "bowphase" 時執行
```yml
AnotherSkill:
  Conditions:
  - stance bowphase
 Skills:
  - ...some bow skills
```