Mechanic: Activate Spawner
--------------------------

在目標位置激活 MythicMobs 刷怪籠 [刷怪籠](Spawners)，因為這項技能而生成的怪物將無視刷怪籠的條件和設定.

細項設定
----------

| 設定項| 簡化寫法| 用途 | 預設值 |
|-----------|------------|----------------------------------------------------------------------------------------------------------------|---------------|
| spawners  | spawner, s | 要激活的生成器的名稱。這也可以使用適當的語法接受群組和佔位符 | NONE          |

  

特別小筆記
-------------

最好與設置"useTimer"屬性結合使用刷怪籠並設置為"false"

範例
--------

這會啟動名為 "BossAdd" 的刷怪籠
```yaml
    Skills:
    - activatespawner{spawner=BossAdd}
```
這會啟動所有在組 "Castle" 內的刷怪籠
```yaml
    Skills:
    - activatespawner{spawner=g:Castle}
```
這會啟動所有名稱前為 "DungeonBoss1Spawner" 的所有刷怪籠 (例如: DungeonBoss1Spawner1, DungeonBoss1Spawner2)
```yaml
    Skills:
    - activatespawner{spawner=DungeonBoss1Spawner*}
    - ...
```