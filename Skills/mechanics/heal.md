Mechanic: Heal
==============

Heals the targeted entity for the specified value. Can also "overheal"
the mob to more than its maximum health.

細項設定
----------

| Attribute  | Aliases | Description| Default |
|------------|---------|-------------------------------------------------------------|---------|
| amount | a   | The amount to heal the target  | 1   |
| overheal* | oh  | Whether or not to apply overhealing as additional MaxHealth | false   |

範例
--------

  Skills:
  - heal{amount=20} @self ~onDamaged 0.2

Heals the casting mob for 20 health (10 hearts) when it is damaged. (20%
chance)

  Skills:
  - heal{amount=20;overheal=true} @self ~onDamaged 0.2

Heals the casting mob for 20 health (10 hearts) when it is damaged. (20%
chance)

If the mob is near or at full health, it will add those 20 health points
onto its existing health. Eg. mob with 20 health using this move will
now have 40 health. 20/20 + 20 = 40/20

The same mob with 17 health will gain 17 health on top of its maximum of
20. 17/20 + 20 = 37/20