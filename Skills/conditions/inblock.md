## 用途
Checks the material at the target location. See the [Spigot Javadoc](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html) for a list of valid materials


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| block | blocks, b, material, mat, m | A list of blocks to match  | |


## 範例
```yaml
  Conditions:
  - inblock{b=WATER,LAVA} false
```


## 簡化寫法
- [x] insideblock