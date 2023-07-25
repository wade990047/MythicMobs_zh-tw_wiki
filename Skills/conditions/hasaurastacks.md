## 用途
Tests if the target has the given range of stacks from an aura


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| auraName  | name, n, aura, buffname, buff, debuffname, debuff, b| The name of the aura to check for ||
| stacks| s | The number/range of stacks to check for | 1   |


## 範例
```yaml
  Conditions:
  - hasaurastacks{n=firedebuff;s=>3} true
```


## 簡化寫法
- [x] hasbuffstacks
- [x] hasdebuffstacks
- [x] aurastacks
- [x] buffstacks
- [x] debuffstacks