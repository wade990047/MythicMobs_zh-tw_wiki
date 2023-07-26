Mechanic: setFaction
=================

Sets or changes the target mob's faction.

細項設定
----------

| Attribute | Aliases| Description | Default Value |
|-----------|------------|----------------------------------------------------------------------------------------------------------------|---------------|
| faction  |  | The name of the faction to apply to the mob. | NONE  |

範例
--------

Skills:
- setFaction{faction=Hostile} @self ~onSpawn

Sets the faction of the mob to "Hostile" when the mob spawns.