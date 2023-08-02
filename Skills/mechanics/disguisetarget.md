用途
========================

改變目標的偽裝樣貌

此技能需要插件 **Libs'Disguises** 以及 **ProtocolLib** 來確保正確運作

查看 [擴充:偽裝](/Mobs/Disguises) 來查詢所有可用的偽裝列表

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------|---------|
| disguise  | d, type | 要應用在目標的偽裝 | |

  

範例
--------

將目標變成羊
```yml
Skills:
  - disguisetarget{d=SHEEP} @target
```

這會將目標轉換為一名玩家並且使用Notch的Skin，頭上的顯示名稱叫做 *Jeb* 且可以使用顏色代碼
```yml
Skills:
  - disguisetarget{d="player libraryaddict setCustomName '&7Jeb' setSkin Notch.png"} @target
```