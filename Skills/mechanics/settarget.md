Mechanic: Set Target
--------------------------
Sets the mob's target to the target entity.
If using threat tables, will increase threat to the threshold to change targets for the targeted entity.

**Attributes**

| Attribute | Alias | Description |
| --------- | ----- | ----------- |
| none  | none  | none|

範例
--------
```yml
  Skills:
  - setTarget @trigger ~onInteract
```