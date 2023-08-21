## 用途
給予玩家金錢. 需要 **Vault** 及其他經濟配合插件

***且必須在config.yml中將Vault啟用***
```yaml
Vault:
  Enabled: true
```

## 細項設定
| 設定項 | 簡化寫法 | 用途  | 預設值 |
|-----------|---------|----------------------|---------|
| amount| a   | 金錢數量 | 0.0 |

  

## 範例
```yaml
  Skills:
  - currencygive{amount=20} @pir{r=20} ~onSpawn 0.2
```