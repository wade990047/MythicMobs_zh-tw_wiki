## 用途
將投射物前方相對於其方向的位置設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| forward   | f, amount, a | 目標點應該向前多遠                        | 1       |
| rotate    | rot       | 目標位置繞著子彈的旋轉角度         | 0       |


## 範例
```yaml
ExampleSkill:
  Skills:
  - projectile{...;
    onTick=[
      - effect:particles{p=flame} @ProjectileForward{f=2}
      - effect:particles @Origin
    ]}
```