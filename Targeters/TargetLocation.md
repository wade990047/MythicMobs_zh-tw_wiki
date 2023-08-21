## 用途
將目標的位置設為目標

> 如果施法者不是玩家，那麼:
>- 如果施法者是具有活動 ThreatTable 的 MythicMob，則將傳回威脅表中威脅最大的實體的位置
>- 如果不滿足上述條件，如果施法者當前處於戰斗狀態，則傳回目標位置
>- 如果不滿足上述條件，將傳回最後一個傷害施法者的實體的位置

## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| maxdistance | max, distance, d | 如果施法者是玩家，則檢查位置的最大距離      | 64       |
| ignoreTransparent | it | 是否應忽略透明方塊                             | true    |

## 範例
```yaml
ExampleSkill:
  Skills:
  - effect:particles @TargetLocation
```


## 簡化寫法
- [x] targetLoc
- [x] TL