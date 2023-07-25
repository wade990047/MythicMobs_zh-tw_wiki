## 用途
Checks the phase of the target Ender Dragon entity.  
A list of valid phases can be found in the [Spigot Phase javadoc](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/entity/EnderDragon.Phase.html).


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| phase | p | A list of phases to match   | |


## 範例
```yaml
  Conditions:
  - enderdragonphase{phase=CIRCLING} true
```
```yaml
Conditions:
- enderdragonphase{phases=FLY_TO_PORTAL,LEAVE_PORTAL} true
```

## 簡化寫法
- [x] edragonPhase