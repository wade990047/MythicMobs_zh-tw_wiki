## 用途 
Creates a particleline ring.  
This mechanic is an extension of the **[Particle effect](/skills/effects/particles)**, and can, as such, **use any of its attributes**.

## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| StartYOffset | syo, ystartoffset, ys | The starting vertical offset  | 0   |
| TargetYOffset | tyo, ytargetoffset, yt | The target vertical offset  | 0   |
| DistanceBetween | db  | The distance between particles  | 1   |
| FromOrigin| fo| Should the mechanic be casted from the origin of the metaskill   | false   |
| RingPoints | rp   | The number of points in the line ring   | 16  |
| RingRadius | rr   | The radius of the line ring | 0.5 |
| maxdistance | md  | The maximum distance for the line   | 256 |


## 範例
```yaml
  Skills:
  - effect:particlelinering{p=flame;r=3;rr=1} @PIR{r=20;limit=1;sort=RANDOM}
```


## 簡化寫法
- [x] particlelinering
- [x] particleringline