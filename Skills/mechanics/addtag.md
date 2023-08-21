用途
================

對目標加上一個記分板標籤

這項技能通常與 **hastag** 一起使用 (可以在 [條件判斷式](/conditions/start) 中找到)

也可以利用原版指令達到一樣的效果

**`/scoreboard players tag <player name> add [Tag Name]`**

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------|---------------|
| tag   | t | 標籤名稱 | default   |

範例
--------

這項技能會為施法者新增名為`Test`的`tag`
```yml
TagSkill:
  Skills:
  - addtag{t=Test} @self
```
這項技能只會在施法者擁有名為`Test`的`tag`時執行
```yml
TagTest:
  Conditions:
  - hastag{t=Test}
 Skills:
  - suicide @self
```