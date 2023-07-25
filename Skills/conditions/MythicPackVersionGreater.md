## 用途
Check if a [Pack](/wikis/Packs) with the specified id is present on the server with a version that is either greater or equal the specified one.


## 細項設定
| Attribute | Alias   | Description   | Default |
|-----------|-------------|--------------------------------------------------------------------|---------|
| packid| pack, id, p | The Pack id to check for  | |
| packversion | packV, version, v | The version to check for  | |


## 範例
```yaml
  Conditions:
  - packversiongreater{p="ThePackId",v="1.2.3"} true
```


## 簡化寫法
- [x] packversiongreater
- [x] packversionisgreater