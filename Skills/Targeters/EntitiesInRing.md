## Description
Targets all entities in a ring around the caster.  
The targeted entities will be the ones at a distance from the caster between the minimum and the maximum range.


## Attributes
| Attribute | Aliases   | Description                                                          | Default |
|-----------|-----------|----------------------------------------------------------------------|---------|
| minrange  | min       | The minimum range of the ring                                        | 5       |
| maxrange  | max       | The maximum range of the ring                                        | 10      |



## Examples
```yaml
  Skills:
  - ignite @EIRR{min=2;max=10}
```


## Aliases
- [x] EIRR