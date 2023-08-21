## 用途
將技能起點附近的隨機位置設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount    | a         | 點的數量             | 5       |
| radius    | r, maxradius, maxr | 最大半徑         | 5       |
| minradius | minr      | 最小半徑         | 0       |
| spacing   | s         | 選定目標之間的最小相隔空間量                | 0       |

## 範例
```yaml
ExampleSkill:
  Skills:
  - projectile{...;
    onEnd=[
      - effect:particles @RandomLocationsNearOrigin{a=10;r=4;minr=1}
    ]}
```


## 簡化寫法
- [x] RLO
- [x] randomLocationsOrigin
- [x] RLNO