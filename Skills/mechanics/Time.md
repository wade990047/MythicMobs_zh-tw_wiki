## 用途
Sets the world's time. Depending on the attributes used, the change in time can be absolute or relative to the target player.

Time mechanics must be synced to function. "sync=true;"

## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| mode  | m | The mode used in the time mechanic. Can be ADD/SET/RESET | ADD |
| amount| ticks, t, amt | The amount of ticks by which the time will be changed| 20  |
| personal  |   | Sets whether to change the global time or the player's client time   | false   |
| relative  |   | Sets whether to keep the player's time synchronized to its world time with an offset  | true|

#### Mode Attribute
The different values the mode attribute can be all have different effects
- **`ADD`** - Sets the current time of the world with an offset
- **`SET`** - Sets the current time of the world
- **`RESET`** - Re-syncs the target's world time with the server world time, if it is not already synced

## 範例
```yaml
#MOB
ExampleMob:
  Type: ZOMBIE
  Skills:
  - sudoskill{s=MidnightAura} @PIR{r=30} ~onTimer:20
```
```yaml
#SKILL
MidnightAura:
  Skills:
  - aura{auraName=midnight;i=1;ms=1;rd=true;
onTick=[
  - time{mode=SET;a=18000;personal=true;relative=false;sync=true} @self
];
onEnd=[
  - time{mode=RESET;sync=true} @self
]} @self
```

## 簡化寫法
- [x] setTime