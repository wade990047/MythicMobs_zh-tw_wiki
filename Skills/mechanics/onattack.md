Mechanic: onAttack
==================

Applies an aura to the target that triggers a skill when they damage
something. Can use any aura attribute

細項設定
----------

| Attribute| Aliases   | Description   | Default Value |
|------------------|---------------|------------------------------------------------------------|---------------|
| onHit| oH| Skill to execute if the target hits something  | NONE |
| cancelEvent  | cE| Whether or not to cancel the event that triggered the aura | false |
| damageAdd| add, a| An optional static increase to the original hit's damage | 0 |
| damageMultiplier | multiplier, m | An optional multiplier on the original hit's damage to the original hit's damage | 1 |

  

範例
--------

  Skills:
  - onAttack{oH=SuperPunch;cE=true;auraname=MyAura}
  - ...