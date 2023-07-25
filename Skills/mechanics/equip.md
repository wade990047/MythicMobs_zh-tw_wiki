## 用途
Equips the mob with an item. Uses the exact same syntax as the
[Equipment](/mobs/equipment) configuration.


## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| item  | items, equipment, equip, e | The item config string to run on the mob.   | |


## 範例
This example would equip the casting mob with a diamond sword.
```yaml
EquipDiamondSword:
  Skills:
  - equip{item=diamond_sword HAND}
```

This example would equip the Skeleton King's crown as a helmet.
```yaml
EquipCrown:
  Skills:
  - equip{item=KingsCrown HEAD}
```