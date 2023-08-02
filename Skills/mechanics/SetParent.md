## 用途

設定目標為施法者的父母 
父母可以是玩家或是其他怪物
配合 [目標選擇器: 父母](/mythiccraft/MythicMobs/-/wikis/Skills/Targeters/Parent) 和 [條件: 父母](/mythiccraft/MythicMobs/-/wikis/skills/conditions/IsParent).

## 範例
如果生物沒有父母，則嘗試將其父母設置為半徑 20 格內最近的 "ZombieBoss"
```yml
ZombieFollower:
  Type: DROWNED
  Skills:
  - setparent @MIR{r=20;t=ZombieBoss;limit=1;sort=NEAREST} ~onTimer:20 ?!hasparent
```