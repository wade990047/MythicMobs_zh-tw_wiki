## 用途
Checks the bow tension of when an entity shoots from a bow


## 細項設定

| Attribute | Aliases  | Description  | Default |
|-----------|------------------|---------------------------------------------------------------|---------|
| force | f, value, v, val | The value of the force/tension to check for. Accepts ranged float values, but only in a range from 0 to 1  | >0  |


## 範例

```yaml
  Conditions:
  - bowtension{value=>0.5} true
```


## 簡化寫法
- [x] bowshoottension