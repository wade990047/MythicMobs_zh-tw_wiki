## 用途
Checks if the target location is near any claims of any supported plugins.  

Supported Plugins:

- GriefPrevention
- Lands
- CrashClaim


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius| r | The given range to check| 16  |


## Example
```yaml
  Conditions:
  - nearclaim{r=20} false
```


## 簡化寫法
- [x] nearClaims