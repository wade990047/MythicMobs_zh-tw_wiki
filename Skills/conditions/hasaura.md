## 用途
Checks if the target entity has the given aura


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| auraName  | name, n, aura, buffname, buff, debuffname, debuff, b| The name of the aura to check for ||


## 範例
```yaml
  Conditions:
  - hasaura{n=firedebuff} true
```


## 簡化寫法
- [x] hasbuff
- [x] hasdebuff