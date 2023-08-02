用途
===============

使怪物在聊天中說話，並提供語言氣泡的選項

**新增於MM v4.10 版**

* 16進位色碼格式 **`<#FFFFFF>`**
* 漸層顏色格式 **`<gradient:#color1:#color2>text</gradient>`**
* 彩虹變色字 **`<rainbow>text</rainbow>`**
* 滑動顯示文字 **`<hover:show_text:'hover text??'>hover over me!</hover>`**
* 可執行指令文字 **`<click:run_command:/say hello>click me!</click>`**

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|---------------|-------------|---------------------------------------------------------------|----------------------------------|
| offset| o   | y軸偏移   | 0.6f|
| radius| r   | 顯示半徑  | 12  |
| maxlinelength | ll, mll, ml | 一行最多幾個字  | 22  |
| lineprefix| lp  | 漂浮文字前綴 | &f  |
| message   | m   | 訊息(影響漂浮文字與聊天室) | NONE|
| chatprefix| cp  | 聊天室前綴 | &lt;caster.name&gt;&f&lt;&co&gt; |
| duration  | d, t| 顯示持續時間(單位:ticks)| MESSAGE LENGTH * 4  |
| sendchatmessage | chatmessage, chat | 是否在聊天室顯示訊息  | true  |

  

範例
--------
```yml
  Skills:
  - speak{offset=0.6f;radius=30;maxlinelength=22;lineprefix="&5";message=" I just spawned!";chatprefix=<caster.name>&f<&co>;duration=200} @self ~onSpawn
  - ...
```