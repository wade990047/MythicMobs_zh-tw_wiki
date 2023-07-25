## 用途
Checks if the target player's inventory slot holds an item that is similar to the specified one.  
To be more specific, their ItemStacks will be compared and the condition will return true if they match.


## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| item  | i, material, m, mm, mythicitem | The item to check for   | DIRT|
| slot  | s | The inventory slot to check for. Accepts 0 to 35, or equipment slots | HAND|


## 範例
Tests the item in slot 0, or the first slot, of the targeted player's inventory.
```yml
  Conditions:
  - itemissimilar{i=MyCustomItem;slot=0} true
```


## 簡化寫法
- [x] issimilar
- [x] similarto