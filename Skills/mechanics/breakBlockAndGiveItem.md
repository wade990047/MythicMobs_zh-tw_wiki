用途
===================================

破壞目標位置的方塊並掉落指定物品.

此技能會掉落任何被破壞的方塊. 必要設定: `forcesync=true`..

細項設定
--------------
| 設定項 | 簡化寫法   | 用途| 預設值 |
|-----------|-----------|------------------------------------|---------------|
| dodrops   | drops, d  | 是否掉落方塊 | true  |
| doeffect  | effect, e | 是否播放方塊破壞特效 | true |
| usetool   | tool, t   | 是否用玩家手中的道具作為破壞標準 | true |
| fakelooting | fl | 是否播放獲取掉落物的動畫 | false |
| items | item, i | 物品列表或是物品掉落集 | |


範例
--------

利用配合 Mythic Crucible 的物品:

只要破壞泥土或是草方塊，則直接給予玩家鑽石，並且不掉落泥土
```yaml
#Items Document
CustomItem:
  Id: GOLDEN_SHOVEL
  Display: 'Lucky Shovel'
  Skills:
  - skill{s=dirtToDiamonds;sync=true} @origin ~onBreakBlock

#Skills Document
dirtToDiamonds:
  TargetConditions:
  - blocktype{t=DIRT,GRASS_BLOCK} true
  Skills:
  - breakBlockAndGiveItem{dodrops=false;items=diamond}
```