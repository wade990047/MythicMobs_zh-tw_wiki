## Mechanic: Propel
Propels the caster of the mechanic towards the target.


## 細項設定

| Attribute  | Aliases | Description   | Default Value |
|----------------|-----------------|----------------------------------------------------|---------------|
| velocity   | magnitude, v| The velocity at which the mob will be propelled.   | 1 |


## 範例
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - propel{v=1;delay=1} @trigger ~onDamaged ?~distance{d=>6}
```