## 用途
Checks is the server is running a specific minecraft version


## 細項設定

| Attribute | Alias   | Description   | Default |
|-----------|-------------|--------------------------------------------------------------------|---------|
| version   | sv, v   | The version to check for  | 1.19.3  |


## 範例
```yaml
  Conditions:
  - serverversion{v="v1.19.4"} true
```

## 簡化寫法
- [x] server
- [x] version