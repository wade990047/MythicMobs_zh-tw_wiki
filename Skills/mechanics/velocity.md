Mechanic: Velocity
==================

Modifies the velocity of the targeted entity(s). May be used on players,
too. Useful for all sorts of things like true knockback resistance,
force-skills or simulated wind.

細項設定
----------

| Attribute | Aliases | Description   | Default Value |
|-----------|---------|-------------------------------------------------------------------------|---------------|
| mode  | m   | The operation to perform. Can be SET, ADD, REMOVE, DIVIDE, or MULTIPLY. | SET   |
| velocityx | vx, x   | Velocity on the x-axis. Can be negative.   | 1 |
| velocityy | vy, y   | Velocity on the y-axis. Can be negative.   | 1 |
| velocityz | vz, z   | Velocity on the z-axis. Can be negative.   | 1 |
| relative  | | If the change in velocity should be relative to the caster's facing direction. In this instance, the `x` axis becomes `forward/backward`, `y` becomes `up/down` and `z` becomes `left/right`| false |

  

範例
--------

This example will stop all momentum of the casting mob upon taking
damage. The effect will only last until the mob decides to move again or
is moved by other sources.

```yaml
internal_mobname:
  Type: Zombie
  Skills:
  - velocity{m=set;x=0;y=0;z=0} @self ~onDamaged
```

While the example above works most of the time, the bow's ARROW_KNOCKBACK enchantment will still manage to move them. This can be prevented by doing a slight modification to the mechanic, as shown below.
```yaml
internal_mobname:
  Type: Zombie
  Skills:
  - velocity{m=set;x=0;y=0;z=0;delay=1} @self ~onDamaged
```