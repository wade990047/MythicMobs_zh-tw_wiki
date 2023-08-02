Mechanic: VariableSkill
===============

Executes another meta-skill like the [Skill mechanic](skills/mechanics/skill), but allows for placeholders inside the skill name


The attribute "sync=true" will be inherited by any sub-skills and cannot
be set to *false* later in a skill-tree.

| Attribute | Shorthand | Description| Default |
|-----------|-----------|---------------------------------------------------------------------|---------|
| skill | s | The metaskill to be executed. Accepts [Placeholders](Skills/Placeholders). |  |
| forcesync | sync  | Whether to force the skill to be run synchroniously with Minecraft. | false   |


範例
--------
```yml
ExampleSkill:
  Skills:
  - vskill{s=ExampleSkill_<random.1to3>} @self

ExampleSkill_1:
  Skills:
  - effect:particles{particle=reddust;color=#FF0000;amount=10}
ExampleSkill_2:
  Skills:
  - effect:particles{particle=reddust;color=#FFFFFF;amount=10}
ExampleSkill_3:
  Skills:
  - effect:particles{particle=reddust;color=#00FF00;amount=10}
```
In the example, the `ExampleSkill` metaskill, once triggered, will execute a skill whose name is composed of `ExampleSkill_` and a randomly generated number between 1 and 3.

#

```yml
Example_StanceSkill:
  Skills:
  - vskill{s=ExampleMob_<caster.stance>_<random.1to2>} @self
```
In this example, the VariableSkill is being used to quickly create some stance-based skills without the need to use any stance conditions and the like

#

```yml
Example_VariablePlaceholder:
  Skills:
  - vskill{s=Fireball_<skill.var.fireballtype>} @self
```
In this example, the VariableSkill mechanic will execute a metaskill whose name depends on some skill-scoped variables that has been set earlier on