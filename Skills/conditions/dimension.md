## 用途
Checks if the target is within a certain dimension.  
A list of valid dimensions can be found in the [Spigot Enviroment javadoc](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/World.Environment.html).


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| dimension | d, environment, env | A list of dimensions to check | THE_END |


## 範例
```yaml
  Conditions:
  - dimension{d=NORMAL} true
```


## 簡化寫法
- [x] environment