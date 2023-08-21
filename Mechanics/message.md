用途
=================

對目標玩家發送訊息，支援 [顏色代碼](/databases/misc/colorcodes) 和 [變量](/skills/stringvariables)

**更新於 v4.10**

* 16進位色碼格式 **`<#FFFFFF>`**
* 漸層顏色格式 **`<gradient:#color1:#color2>text</gradient>`**
* 彩虹變色字 **`<rainbow>text</rainbow>`**
* 滑動顯示文字 **`<hover:show_text:'hover text??'>hover over me!</hover>`**
* 可執行指令文字 **`<click:run_command:/say hello>click me!</click>`**

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-----------------------------|---------|
| message   | msg,m   | 要傳送的訊息| None|
| audience  | | 訊息目標 | |

---------------

訊息目標設定更新於 v4.12

可用的目標有: caster, target 和 world.

範例
--------
```yaml
  Skills:
  - message{m="<mob.name>&f<&co> Hahaha! You will all die!"} @PlayersInRadius{r=30}
```