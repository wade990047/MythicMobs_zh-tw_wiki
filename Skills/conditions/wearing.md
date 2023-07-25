## 用途
This condition checks if the target entity is wearing the selected item.  


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| armorslot | slot, s   | The item slot to check. | HEAD|
| material  | mat, m, mythicmobsitem, mmitem, mmi, item | A material or MythicItem name to check for. Also supports MMOItems in the format mmoitems.TYPE.ID  | DIRT|

**Valid Slots:**

| HEAD | CHEST | LEGS | FEET | HAND | OFFHAND |   
| ---- | ----- | ---- | ---- | ---- | ------- |  


## 範例
```yaml
Conditions:
  - wearing{slot=HAND;m=IRON_SWORD} true
  - wearing{slot=CHEST;m=mmoitems.TYPE.ID} true
```


## 簡化寫法
- [x] iswearing 
- [x] wielding 
- [x] iswielding