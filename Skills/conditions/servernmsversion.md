## 用途
Checks is the server is running a specific minecraft NMS version


## 細項設定

| Attribute | Alias   | Description   | Default |
|-----------|-------------|--------------------------------------------------------------------|---------|
| version   | sv, v   | The version to check for   | v1_19_R1_2 |


## 範例
```yaml
  Conditions:
  - nmsversion{v="v1_19_R1"}
```

## 簡化寫法
- [x] servernms
- [x] nmsversion