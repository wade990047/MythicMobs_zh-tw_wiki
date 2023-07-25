## 用途
Teleports the caster up or down.  
The skill will attempt to find a safe landing location and should generally avoid putting the mob inside of blocks.  
No target is required for this mechanic, as the caster will always be the one that is teleported.

## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| y |   | The distance to teleport on the y axis  | 0   |


## 範例
This example would teleport the caster 5 blocks up.
```yaml
WarpY:
  Skills:
  - teleportY{y=5}
```


## 簡化寫法
- [x] tpy