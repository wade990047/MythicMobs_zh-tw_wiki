用途
========================

對目標玩家發送隨機訊息(符號 "#" 會使技能失效)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------------------------------------------------------------------------------|---------------|
| messages  | m   | 要發送的訊息列表 |   |

範例
--------
```yml
Skills:
  - randommessage{
  m=
  "message 1",
  "message 2",
  "message 3";
  } @PIR{r=20} ~onInteract
```
```yml
Skills:
- randommessage{m="one test","not a test","test";} @PIR{r=20} ~onInteract
```