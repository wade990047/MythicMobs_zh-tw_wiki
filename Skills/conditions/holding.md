## 用途
Checks if the target is holding a given material


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| material  | m, type, t| A material or MythicItem internal id to check for| |


## 範例
```yaml
# Make sure you use all caps for materials, otherwise the console will say it is not a valid material!
  Conditions:
  - holding{m=DIAMOND_SWORD} true
```