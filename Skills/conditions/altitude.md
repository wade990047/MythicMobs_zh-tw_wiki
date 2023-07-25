## 用途
This condition tests how far above the ground the target entity is.

## 細項設定

| Attribute | Aliases| Description| Default |
| --------- | -------------  | ------------------------------------------------------- | ------- |
| height| altitude, a, h | The height range to check  | |
| maxHeight | mH | Limits the maximum height this condition can checks for | 30  |


## 範例

```yaml
Conditions:
- altitude{h=3-5} true
```

## 簡化寫法
- [x] heightfromsurface