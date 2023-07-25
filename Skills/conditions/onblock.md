## 用途
Matches the block the target entity is standing on.  
A list of available materials can be found on the [Spigot Javadoc].(https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html) 


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| material  | m, type, block, b | A list of materials. The condition will match if one is found| STONE   |


## 範例
```yaml
  TargetConditions:
  - onblock{m=BEDROCK,OAK_LEAVES,ACACIA_FENCE} false
```

```yaml
  TargetConditions:
  - onblock{m=DIRT,STONE,GRAVEL} true
```