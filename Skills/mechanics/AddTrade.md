## 用途
改變村民的交易內容，如果村民在使用這個技能時沒有任何職業，他就會變成傻子


## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| action| mode, m   | 要做的變更，可以是 `ADD`, `REMOVE`,`REPLACE`  | ADD |
| slot  | s , index | 要變更的欄位，起始值是 0| 0   |
| ingredient| item, ingredient1, item1, i, i1 | 第一個需求物品   | STONE   |
|ingredient2| item2, i2 | 第二個需求物品   | |
| result| r | 交易後獲得的物品| STONE   |
| maxUses   | uses, u   | 可以使用的次數   |<Max Int>|
| experienceReward | expReward, exp, dropExp | 交易是否掉落經驗 | false   |
| priceMultiplier|multiplier|當玩家使村民生氣後的交易倍率 |0 |
| demand| d | 交易的需求量 | 1   |
| specialPrice | special| 村民對玩家友好時的特價 (拯救村民或村莊英雄的效果) | 1   |
| ignoreDiscounts | discounts | 是否忽略折扣| false   |


## 範例
```yml
TestVillager:
  Type: Villager
  Display: 'OwO'
  Skills:
  - addTrade{item=DIAMOND 1;item2=EMERALD 2;result=IRON_INGOT 3;expReward=True;villExp=999;multiplier=0} @self ~onDamaged
  - addTrade{action=REPLACE;slot=1;item=DIRT 1;item2=COAL 2;result=DIAMOND_BLOCK 3;expReward=True;villExp=999;multiplier=0} @self ~onSignal:rev
```


## 簡化寫法
- [x] setTrade
- [x] removeTrade
- [x] replaceTrade