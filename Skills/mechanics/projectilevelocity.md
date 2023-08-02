# Mechanic: Velocity

Modifies the velocity of the calling [Projectile](/skills/mechanics/projectile) or [Missile](/skills/mechanics/missile). In this context, it works the same as the [Velocity](/skills/mechanics/velocity) mechanic.


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|-------------------------------------------------------------------------|---------------|
| mode  | m   | The operation to perform. Can be SET, ADD, REMOVE, DIVIDE, or MULTIPLY. | SET   |
| velocityx | vx, x   | Velocity on the x-axis. Can be negative.   | 1 |
| velocityy | vy, y   | Velocity on the y-axis. Can be negative.   | 1 |
| velocityz | vz, z   | Velocity on the z-axis. Can be negative.   | 1 |
| relative  | | If the change in velocity should be relative to the projectile's facing direction. In this instance, the `x` axis becomes `forward/backward`, `y` becomes `up/down` and `z` becomes `left/right`| true |


## 範例
```yml
Projectile-onTick:
  Conditions:
  - chance{chance=0.1} true
  Skills:
  - projectilevelocity{mode=ADD;vz=0.3}
```