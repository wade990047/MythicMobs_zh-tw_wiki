## 用途
Checks if the target entity's equipped item has an enchantment. A list of valid enchantments can be found in the [Spigot Javadoc](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/enchantments/Enchantment.html).


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
|enchantment|type, ench, e, t| The enchantment to test for| ANY |
| level | lvl, l| The level to test for   | >0  |


## 範例:
```yaml
  TargetConditions:
  - hasenchantment{e=DAMAGE_ALL;l=>3} true
```


## 簡化寫法
- [x] hasEnchant