## 用途
Matches the last signal received by the target mob


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| signal| s | The signal to match | DEFAULT |


## 範例
```yaml
  Conditions:
  - lastsignal{s=fireCannonShot} true
```