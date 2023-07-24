## Description
Sets the "Parent" of the casting MythicMob as the targeted entity.  
The Parent can be either a Player or another MythicMob.
Works with the [@Parent Targeter](/mythiccraft/MythicMobs/-/wikis/Skills/Targeters/Parent), and the [IsParent Condition](/mythiccraft/MythicMobs/-/wikis/skills/conditions/IsParent).

## Attributes
>*This mechanic has no attributes*


## Examples
This mob will try to set its current parent to the nearest ZombieBoss mob in a 20 block radius if it does not already have a parent
```yaml
ZombieFollower:
  Type: DROWNED
  Skills:
  - setparent @MIR{r=20;t=ZombieBoss;limit=1;sort=NEAREST} ~onTimer:20 ?!hasparent
```