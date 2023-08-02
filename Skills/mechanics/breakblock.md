用途
=====================

破壞目標位置的方塊

此技能會掉落任何被破壞的方塊. 必要設定: `forcesync=true`.

細項設定
----------

| 設定項 | 簡化寫法   | 用途| 預設值 |
|-----------|-----------|------------------------------------|---------------|
| doDrops   | drops, d | 是否掉落方塊 | true  |
| doEffect  | efffect, e | 是否播放方塊破壞特效 | true |
| useTool   | tool, t | 是否用玩家手中的道具作為破壞標準 | true |

doDrops, doEffect, 和 useTool 都是從 MM v4.12 後新增

----------
筆記:

下方測試技能可以使用指令 /mm test cast TestingBreakBlock

1. 當玩家手上**沒有拿**物品，破壞方塊時不掉落物品也不播放特效
```yml
TestingBreakBlock:
  Skills:
  - breakblock{forcesync=true;doEffect=true;doDrops=true;useTool=true} @origin
```

2. 當玩家手上**沒有拿**物品，破壞方塊時掉落物品但不播放特效 
```yml
TestingBreakBlock:
  Skills:
  - breakblock{forcesync=true;doEffect=true;doDrops=true;useTool=false} @origin
```

3. 當玩家手上**有拿**物品，破壞方塊時掉落物品但不播放特效
```yml
TestingBreakBlock:
  Skills:
  - breakblock{forcesync=true;doEffect=false;doDrops=true;useTool=true} @origin
```

4. 當玩家手上**有拿**物品，破壞方塊時不掉落物品也不播放特效
```yml
TestingBreakBlock:
  Skills:
  - breakblock{forcesync=true;doEffect=true;doDrops=false;useTool=true} @origin
```

5. 當玩家手上**有拿**物品，破壞方塊時掉落物品也播放特效
```yml
TestingBreakBlock:
  Skills:
  - breakblock{forcesync=true;doEffect=true;doDrops=true;useTool=true} @origin
```
--------

範例
--------

當點擊右鍵時會在當前世界座標 x:100,y:64,z:100 破壞方塊
```yml
Skills:
  - breakblock{forcesync=true} @location{c=100,64,100} ~onInteract
```