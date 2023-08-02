Mechanic: SetScore
==================

*Added in version 2.3*

為 變更計分板數值 of a fake player name. Works
like the [Modify Score](/skills/mechanics/modifyscore) mechanic, but is
only capable of performing the **set**-action.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------|---------|
| objective   | obj, o  | 記分板名稱，若不存在則自動創建 | |
| value   | v   | 要使用的數值   | |
| name, entry | n, e| The name of the fake player | dummy   |

  
範例
----

This example will set the score of a player named
"Bob" for the objective "TestScore", even if that player doesn't exist
on the server.  
It will create the objective if it does not currently exist.

  Skills:
  - setscore{o=TestScore;e=Bob;v=1} ~onInteract 

![](https://i.imgur.com/0HKvAUM.png)