## 用途
Checks the cause of the damage the entity took, if the skilltree originated from a [onDamaged Trigger](/Skills/Triggers#ondamaged) or an [onDamaged Aura](/skills/mechanics/ondamaged).  
A list of valid damage causes can be found in the [Spigot DamageCause javadoc](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/entity/EntityDamageEvent.DamageCause.html).


## 細項設定

| Attribute | Aliases   | Description   | Default   |
|-----------|-----------|----------------------------------------------------------------|---------------|
| damagecause | cause, c | The damage cause to match| ENTITY_ATTACK |


## 範例
```yaml
  Conditions:
  - damagecause{cause=ENTITY_ATTACK} true
```