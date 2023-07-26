Mechanic: togglesitting
=======================

**Aliases:** sit

Toggles the sitting state for cats, dogs, foxes, and parrots.

細項設定
----------

| Attribute | Aliases   | Description| Default Value |
|-----------|-----------|------------------------------------|---------------|
| setSitting | state| Sets the sitting state | false |

範例
--------
```
Dog:
  Type: Wolf
  Skills:
  - sit{state=true} @Self ~onInteract
```