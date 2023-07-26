## 用途

Shoots a volley of arrows or item-projectiles at the targeted entity or
location that deals damage. Can use any attribute from the Shoot
mechanic.

## 細項設定

| 設定項 | 簡化寫法 | 用途  | 預設值 |
|-----------|---------|---------------------------------------------------|---------|
| amount| a   | The amount of projectiles | 10  |
| source| s   | The type of the volley. Can be REGULAR or RAIN| REGULAR |
| radius| r   | The radius of the volley  | 0   |
| yoffset   | y   | The y offset of the target location of the projectiles | 0  |
| canPickup   | pickup  | Whether the arrows can be picked up by players | true|

## 範例
```yaml
  Skills:
  - volley{type=EGG;velocity=5;damage=10;amount=20}
```

## 簡化寫法
- [x] shootvolley