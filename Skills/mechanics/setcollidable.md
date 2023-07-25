## Mechanic: SetCollidable
Sets if the target of the mechanic should have a collidable hitbox or not.
<br>The result is equivalent to the [Collidable](/Mobs/Options#collidable) Option.

## 細項設定
| Attribute  | Aliases | Description   | Default Value |
|----------------|-----------------|----------------------------------------------------|---------------|
| collidable | state, value, c | Sets if the mob is collidable or not   | false |

## 範例
In this example, the mob will permanently become not collidable once it receives a source of damage
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - setcollidable{c=false} @self ~onDamaged
```
##
In this example, the mob will apply an aura to itself. For the duration of the aura, the mob will be non collidable.
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - aura{d=100;rd=true;ms=1;
onStart=[
- setcollidable{c=false} @self
];
onEnd=[
- setcollidable{c=true} @self
]} @self ~onDamaged
```