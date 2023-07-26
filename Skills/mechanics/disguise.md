用途
==================
改變施法者的偽裝樣貌

對目標執行偽裝設定字串. 

此技能需要插件 **Libs'Disguises** 以及 **ProtocolLib** 來確保正確運作

查看 [擴充:偽裝](/Mobs/Disguises) 來查詢所有可用的偽裝列表

細項設定
----------

| 設定項 | 簡化寫法 | 用途   | 預設值 |
|-----------|---------|-----------------------------------|---------|
| disguise  | d, type | 施法者的偽裝樣貌. | |

  

範例
--------

你可以用指令 ``/mm test cast TestingDisguiseMechanic`` 測試下方的技能

這項偽裝會使你變成羊，同時正在燃燒以及旋轉
```yml
TestingDisguiseMechanic:
  Skills:
  - disguise{d="Sheep SetBurning SetSpinning"} @self
```
