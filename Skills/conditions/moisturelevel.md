## 用途
Checks if the target block of farmland has the specified level of hydratation.

- `0` means that the farmland is not hydratated
- `1-6` means that a once hydratated farmland is gradualy losing its hydratation after removing its access to water
- `7` is for a fully hydratated farmland.


## 細項設定
| Attribute | Alias   | Description   | Default |
|-----------|-------------|--------------------------------------------------------------------|---------|
| l | | The level of hydratation to check for | |

Examples
---
```yml
  TargetConditions:
  - moisturelevel{l=3} true
```
```yml
  TargetConditions:
  - moistureness{l=1to6} true
```

## 簡化寫法
  - [x] moistureness