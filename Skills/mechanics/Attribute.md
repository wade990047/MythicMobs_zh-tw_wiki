## Description
Sets the base value of the targeted entity's attribute


## Attributes

| Attribute | Aliases   | Description                                                          | Default |
|-----------|-----------|----------------------------------------------------------------------|---------|
| attribute | attr      | The attribute to set                                            | GENERIC_LUCK |
| amount    | amt, a    | The amount of the attribute                                          | 0     |
| duration  | dur       | The duration of the attribute                                          | 0     |


## Examples
```yaml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - attribute{attribute=GENERICK_LUCK;a=2;d=1200} @trigger ~onDeath
```


## Aliases
- [x] setattribute