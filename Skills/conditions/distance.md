## 用途
Whether the distance between the caster and target is within the given range.  
Can be a single number, a ranged value (20to40), or >10 <5, etc.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| distance  |   d   | The distance to match   | |


## 範例
```yaml
  TargetConditions:
  - distance{d=<2}
```