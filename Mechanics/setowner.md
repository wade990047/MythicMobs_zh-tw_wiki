## 用途
設定目標為施法者的擁有者

這是 MythicMobs 中使用的特殊屬性，與普通生物的"普通"擁有者不同。
配合 [目標選擇器:擁有者](/Skills/Targeters/Owner) 和 [條件: 擁有者](/skills/conditions/owner).  

如果目標怪物是 `Wolf`,`Cat`,`Parrot` 也會同時將原版的擁有者一起設定


## 範例
```yml
PetSheep:
  Mobtype: sheep
  Display: 'Pet'
  Health: 20
  Damage: 18
  Skills:
  - skill{s=SetOwner} @trigger ~onInteract
  - skill{s=HealOwner} @PIR{R=10} ~onTimer:50
```

將互動者做為主人
```yml
SetOwner:
  Skills:
  - setowner @trigger
```
這項技能只會恢復主人血量
```yml
HealOwner:
  TargetConditions:
  - owner true
  Skills:
   - heal{a=10}
```