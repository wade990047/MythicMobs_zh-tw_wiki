Mechanic: Look
--------------

Causes the entity to look at it's target. Can be used to make cool
effects or creepy ones depending on how creative you get with it.

細項設定
----------

| Attribute   | Aliases | Description| Default Value |
|-------------|---------|----------------------------------------------------------------------------------|---------------|
| headOnly| | Only the mob's head is facing the target.   | true  |
| immediately | | Immediately causes the mob to turn towards the target with no turning animation. | false |

範例
--------

CreepyStare:
  Skills:
  - look{headOnly=true;immediately=true} @Target

The skill above causes the mob to immediately force it's head to face
the target immediately. Giving it a creepy effect as only the head will
stare for a short bit before the body catches up and turns around as
well.
