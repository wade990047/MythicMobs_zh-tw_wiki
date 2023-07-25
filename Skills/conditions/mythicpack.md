## 用途
Check if a [Pack](/wikis/Packs) with the specified id is present on the server.


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| packid| pack, id, p | The pack id to check for  | |


## 範例
```yaml
  Conditions:
  - mythicpack{p="ThePackId"} true
```


## 簡化寫法
- [x] pack
- [x] haspack