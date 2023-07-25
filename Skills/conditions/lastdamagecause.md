## 用途
Checks the target's last damage cause.  
You can find a list of valid damage causes on the [Spigot Javadoc](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/entity/EntityDamageEvent.DamageCause.html)


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| damagecause | cause, c | The damage cause to match| ENTITY_ATTACK |


## 範例
```yaml
  Conditions:
  - lastdamagecause{c=ENTITY_ATTACK} true
```