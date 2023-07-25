Goal: meleeAttack
--------------

Causes the mob to move to and melee attack its target

### 細項設定

| Attribute | Aliases | Description | Default |
|-----------|---------|-------------------------|:-------:|
| speed | s   | Movement speed modifier |1|




### 範例

```yaml
ExampleMob:
  Type: Skeleton
  AIGoalSelectors:
- clear
- meleeattack{speed=1}
```