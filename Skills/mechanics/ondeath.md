Mechanic: onDeath
==================

Applies an aura to the target that triggers a skill when they die

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|------------------|---------------|------------------------------------------------------------|---------------|
| onDeathSkill| od| Skill to execute if the target dies| NONE |


範例
--------

Force an onDeath aura through sudoskill on all entities around you. When you kill them they will all drop diamonds. This could be useful for quests where killing enemies makes them drop a quest item, but you dont want to have to add the drop mobs. 

ForceApplyAura:
  Skills:
  - sudoskill{s=ApplyAura} @EIR{r=50}
ApplyAura:
  Skills:
  - onDeath{od=DropDiamonds;auraname=Gonners;d=1200;i=1} @self
DropDiamonds:
  Skills:
  - dropitem{i=DIAMOND 3-5} @self