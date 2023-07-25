## 用途
Matches if the target location is inside of a structure. Supports wildcards and structures from datapacks.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| structure | structures, s | The structure to check for. Can be a list.   | village |


## 範例
```yml
  Conditions:
  - structure{s=minecraft:desert_pyramid} true
```