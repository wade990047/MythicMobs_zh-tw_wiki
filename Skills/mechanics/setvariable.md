Mechanic: SetVariable
=====================

Sets a [variable](/skills/variables). Variables can be permanent or
temporary, and can be used in conjunction with conditions or
placeholders to store data.

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------|
| variable  | name, n, var, key, k | The name of the variable. Can optionally be prefixed with **scope.**   |   |
| value | val | The value to set the variable to. Must be applicable for **type** or the mechanic will fail. Should be surrounded in double-quotes if using spaces. Value can also include placeholders, even from PlaceholderAPI. |   |
| scope | s   | The [scope](/skills/variables#variable_scopes) of the variable, e.g. where the variable will be located.| SKILL |
| type  | t   | The [type](/skills/variables#variable_types) of the variable. Set to STRING if you are using text instead of numbers.| INTEGER   |
| save  | | Whether the variable should save between reloads, reboots and disconnects. Does not apply to SKILL-scoped variables.| false |
| duration  | d   | How long (in ticks) the variable should last. Does not apply to SKILL-scoped variables.| Infinite  |

  
Examples
----

In this example, the target players would only hear growling from any
number of nearby bears once every 10 minutes.

BearMob:
  Skills:
  - skill{s=BearGrowl} @PlayersInRadius{r=40} ~onTimer:60

BearGrowl:
  TargetConditions:
  - variableEquals{var=target.heardbear;value="yes"} cancel
  Skills:
  - message{m="&7You hear a growling noise..."}
  - setvariable{var=target.heardbear;value="yes";type=STRING;duration=6000}

In this example, the extra "IgnitionDamage" skill would only fire if the
"do_ignite" variable were set on the skill tree.

Strike:
  Skills:
  - setvariable{var=skill.do_ignite;type=STRING;value="yes"} 0.5
  - damage{amount=20}
  - skill{s=IgnitionDamage}

IgnitionDamage:
  Conditions:
  - varEquals{var=skill.do_ignite;value="yes"}
  Skills:
  - ignite{ticks=20}
  - effects:particles{}

In this example is a placeholder from MMOItems being stored inside a int/float variable.

PlaceholderDamage:
  Skills:
  - setvariable{var=caster.new_skill_damage;value="%mmoitems_stat_skill_damage%";type=INTEGER} @self
  - damage{a="100 * <caster.var.new_skill_damage>"} @PIR{r=5}

Also,other variables can be stored inside a int/float variable.

VariableSend:
  Skills:
  - setvariable{var=caster.VariableA;value="%mmoitems_stat_skill_damage%";type=INTEGER} @self
  - setvariable{var=caster.VariableB;value="<caster.var.VariableA> * 2";type=INTEGER} @self
  - setvariable{var=caster.VariableC;value="<caster.var.VariableA> + <caster.var.VariableB>";type=INTEGER} @self

Extra Information
----------------

- [x] Alias: setvar