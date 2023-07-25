## 用途
Tests if the entity type of the target is the specified one.  
A list of valid entity types can be found on the [Spigot Javadocs](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/entity/EntityType.html).

## 細項設定

| Attribute | Alias| Description |
| --------- | -------- | ------------------------------- |
| type  | types, t | A list of entity types to match |

## 範例

```yaml
Conditions:
- entitytype{t=ZOMBIE} true
```

```yaml
TargetConditions:
- entitytype{t=WITCH} true
```

```yaml
TriggerConditions:
- entitytype{t=PLAYER} true
```

## 簡化寫法
- [x] mobtype