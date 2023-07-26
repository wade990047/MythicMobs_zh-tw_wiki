Mechanic: AddTag
================

Adds a scoreboard tag to the target.

細項設定
----------

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|---------|----------------------------|---------------|
| tag   | t   | The string-name of the tag | default   |

  

Special Notes
-------------

This is used in conjunction with the **hastag condition** (see
[Conditions](/conditions/start)). You can also use the vanilla command
"/scoreboard players tag &lt;player name&gt; add [Tag Name] " to do
the same thing.

範例
--------

This skill would give the casting mob the tag "Test".

TagSkill
  Skills:
  - addtag{t=Test} @self

This skill would only run on the mob if it had the tag, "Test".

TagTest:
  Conditions:
  - hastag{t=Test}
 Skills:
  - suicide @self
