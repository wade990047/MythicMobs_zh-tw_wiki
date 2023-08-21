## 用途
設置目標是否應該有可碰撞的碰撞箱
<br>結果相同於 [Collidable](/Mobs/Options#collidable) 設定項

## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|----------------|-----------------|----------------------------------------------------|---------------|
| collidable | state, value, c | 是否要擁有碰撞箱   | false |

## 範例
受傷後怪物將沒有可碰撞的碰撞箱
```yml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - setcollidable{c=false} @self ~onDamaged
```
##
受傷後5秒內怪物沒有可碰撞的碰撞箱
```yml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - aura{d=100;rd=true;ms=1;
onStart=[
- setcollidable{c=false} @self
];
onEnd=[
- setcollidable{c=true} @self
]} @self ~onDamaged
```