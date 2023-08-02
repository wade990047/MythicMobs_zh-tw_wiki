用途
======================

對目標玩家送出一則 JSON 格式的訊息
JSON 訊息能夠處理特殊事件、點擊事件和其他一些功能，這些在其他訊息技能中不可用。

並且支持[顏色代碼](/databases/misc/colorcodes) 和 [消息變量](/skills/stringvariables)。

JSON 訊息的格式比0日常使用的消息格式要高級/難設定，語法需要一些額外的符號。如果你不知道有關編寫 JSON 的任何訊息

可以到[這裡](https://www.minecraftjson.com/) 與 [這裡](http://minecraft.tools/en/tellraw.php) 查詢資料

**注意，雙引號必須替換為單引號JSON 訊息技能。**

不要在回報錯誤中回報與此技能相關的問題，除非你確定你的語法正確。

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-|---------|
| message   | m   | 要傳送的JSON訊息. 必須由雙引號(")包圍 | |

  

範例
--------

可以使用 bukkit 顏色代碼或 json 顏色格式:  
```yml
  Skills:
  - jsonmessage{m="[{'text':'&aHey, i am a JSON message!'}]"} @trigger ~onInteract
  - jsonmessage{m="[{'text':'Hey, i am a red JSON message!','color':'red'}]"} @trigger ~onInteract
```

---------

這是如何使用特殊事件的範例:  
  
<img src="http://fs5.directupload.net/images/160309/7irfoune.jpg" width="500" height="30" alt="http://fs5.directupload.net/images/160309/7irfoune.jpg" />

```yml
  Skills:
  - jsonmessage{m="[{'text':'&7With me, you can create hover events','hoverEvent':{'action':'show_text','value':{'text':'&aI am a hover event :)'}}}]"} @trigger ~onInteract
```

---------

點擊事件可以這樣創建，可以透過指令 /mm signal 創建交互式任務怪物。

這個範例中，如果玩家與怪物互動，怪物發送JSON訊息給玩家後，若玩家點擊訊息則將向指定怪物發送信號。
  
![](http://fs5.directupload.net/images/160309/gjxvhpd8.jpg)
```yml
  Skills:
  - jsonmessage{m="[{'text':'&7&nAlso click events! :)','clickEvent':{'action':'run_command','value':'/mm signal <mob.uuid> <signal>'}}]"} @trigger ~onInteract
```