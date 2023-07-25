## 用途
Matches how many players the target mob has killed.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| kills | k | The number range to match   | 0   |


## 範例

```yaml
  Conditions:
  - playerkills{k=>10} true
```