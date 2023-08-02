用途
=======================

![](http://fs5.directupload.net/images/160306/zswobuo8.jpg)

對目標玩家送出提示欄訊息

支援 [顏色代碼](/databases/misc/colorcodes) 和 [變量](/skills/stringvariables)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|----------------------------------------------------|---------|
| message   | m   | 要傳送的訊息必須被 (") 包圍 | |

範例
--------
```yml
Skills:
- actionmessage{m="<mob.name>&f is casting a spell!"} @PlayersInRadius{r=30}
- actionmessage{m="&lHello! &cI'm &athe &9&lactionmessage-bar&r! &e:)"} @trigger ~onInteract
- am{m="<mob.name>&f is using the *skill alias!*"} @PlayersInRadius{r=30}
```