## 用途 
Creates a cloud of particles around the target location

## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| particle  | p | The particle effects to use | reddust |
| type  | effect, t | The type of the effect given by the cloud| SLOW|
| potionduration | pd   | The duration of the potion effect   | 100 |
| level | lvl, l| The level of the potion effect  | 1   |
| duration  | d, cloudduration | The duration of the particle cloud| 200 |
| durationreductiononuse  | drou | The duration reduction for the cloud on use | 0   |
| radius| r | The radius of the cloud | 2   | 
| radiusreductiononuse | rrou | The radius reduction for the cloud on use  | 0   |
| radiusreductionontick | rrot | The radius reduction for the cloud per tick   | 0   |

### Particle Attribute

A list of particle types can be found **[here](/skills/effects/particles/types)**. 

[All of the spigot particle effects listed in the javadocs should be acceptable as well.](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Particle.html)


## 範例
```yaml
  Skills:
  - summonareaeffectcloud{d=600;r=20;rrot=1} @self
```


## 簡化寫法
- [x] summonCloud