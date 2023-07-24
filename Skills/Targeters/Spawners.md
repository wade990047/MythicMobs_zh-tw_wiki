## 用途
將指定刷怪籠的位置設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| spawners  | spawner, s| 刷怪龍的名稱 可以是名稱, 群組 (`g:groupname`) 或包含通用符 (`Spawner` 相當於 *Spawner1*,*Spawner2*,*Spawner3*...)                |         |


## 範例
```yaml
ExampleSkill_SingleSpawner:
  Skills:
  - effect:particles @Spawner{s=TestSpawner}
```
```yaml
ExampleSkill_Group:
  Skills:
  - effect:particles @Spawner{s=g:ExampleSpawnerGroup}
```
```yaml
ExampleSkill_WildCard:
  Skills:
  - effect:particles @Spawner{s=ForestSpawner_*}
```