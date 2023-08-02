用途
--------------------------

停止玩家使用物品，例如盾牌，如果要使用冷卻可以配合aura

範例
--------
```yml
Skills:
  #基本做法
  - stopusingitem{} @NearestPlayer
  
  #利用光環當玩家舉盾時取消舉盾
  - aura{onTick=[ - stopusingitem{} ?isBlocking ];duration=500} @NearestPlayer
```