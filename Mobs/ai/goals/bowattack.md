Goal: bowAttack
--------------
*Aliases*: skeletonbowattack, bowshoot, bowmaster

An advanced ranged attack that can often cause the shooter to strafe backwards or clockwise.

### 細項設定

| Attribute  | Aliases  | Description | Default |
|----------------|----------|-------------------------|:-------:|
| speed  | s| Movement speed modifier |1|
| attackspeedmin | amin | Minimum attack interval |   20|
| attackradius   | radius,r | |   15|

### 範例

```yaml
ExampleMob:
  Type: Skeleton
  AIGoalSelectors:
- clear
- bowattack{speed=1;amin=20;radius=15}
```