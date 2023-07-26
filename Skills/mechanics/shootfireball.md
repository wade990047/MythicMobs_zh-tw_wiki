Mechanic: Shoot Fireball
========================

Shoots a fireball from the mob towards the target entity or location.
**Caution** the large version of this fireball can grief blocks.

細項設定
----------

| Attribute | Aliases   | Description  | Default Value |
|---------------|-----------|--------------------------------------------------------------------------------|---------------|
| yield | y | The yield (power) of the fireball's explosion.| 1 |
| velocity  | v | The velocity of the fireball. | 1 |
| incendiary| i | (true/false) Whether the fireball will leave behind fire.  | false |
| fireTicks | ft| How long (in ticks) fire left behind by the fireball will persist. | 0 |
| smallfireball | small,sml | Whether or not to use the smaller blaze fireball instead of the ghast fireball | false |
| playsound | ps| Whether or not to play the fireball launching sound when it is created | false |
| type  | t  | SMALL/LARGE/DRAGON Added in MM 4.11 | SMALL |

  

範例
--------

This example would shoot a barrage of 3 fast-moving fireballs at the
target.
```yaml
FireballBarrage:
  Skills:
  - shootfireball{y=1;v=4} @target
  - delay 10
  - shootfireball{y=1;v=4} @target
  - delay 10
  - shootfireball{y=1;v=4} @target
```