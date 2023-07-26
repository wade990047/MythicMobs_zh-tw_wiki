Mechanic: ModifyMobScore
===========================

Modifies the scoreboard-objective value of the fake casting mob.

A list of possible operations for the action-syntax:

-   SET
-   ADD
-   SUBTRACT
-   MULTIPLY
-   DIVIDE
-   [1] MOD

細項設定
----------

| 設定項 | 簡化寫法 | 用途  | 預設值 |
|-----------|---------|----------------------------------------------------------------------------------------------------------------------------------|---------|
| objective | obj, o  | Specifies the scoreboard objectiv to be changed. If the objective doesn't exist it will automatically be created by the mechanic | |
| action| a   | The operation to perform  | ADD |
| value | v   | The value to perform the operation with   | |

  
Examples
----
```yaml
- modifymobscore
{
objective=someobjective;
action=multiply;
v=2
} ~onAttack
```
[1] shorthand for "Modular Division"