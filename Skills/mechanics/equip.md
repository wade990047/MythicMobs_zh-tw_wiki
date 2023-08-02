## 用途
讓施術者裝備指定物品，和[裝備](/mobs/equipment) 有著相同設定項


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| item  | items, equipment, equip, e | 裝備設定   | |


## 範例
讓怪物手拿鑽石劍.
```yml
EquipDiamondSword:
  Skills:
  - equip{item=diamond_sword HAND}
```

讓怪物頭戴 "KingsCrown"
```yml
EquipCrown:
  Skills:
  - equip{item=KingsCrown HEAD}
```