## 用途
變更時間，可以變更當前世界的時間，也可以獨立變更目標玩家的顯示時間

技能必要設定項`sync=true`

## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|------------------|---------|
| mode  | m | 變更時間的方法，可以是： `ADD/SET/RESET` | ADD |
| amount| t | 要變更的時間量(單位: ticks)| 20  |
| personal  |   | 是否獨立變更玩家的時間 | false   |
| relative  |   | 設置是否讓玩家的時間與其世界時間保持同步(含偏移量)  | true|

#### 變更方法
以下是各方法的解釋
- **`ADD`** - 設置基於當前世界時間的額外偏移時間(增加意義)
- **`SET`** - 設置當前的世界時間
- **`RESET`** - 重置目標的世界時間，若未完成同步可用此方法修正

## 範例
```yml
ExampleMob:
  Type: ZOMBIE
  Skills:
  - sudoskill{s=MidnightAura} @PIR{r=30} ~onTimer:20
```
---
```yml
MidnightAura:
  Skills:
  - aura{auraName=midnight;i=1;ms=1;rd=true;
onTick=[
  - time{mode=SET;a=18000;personal=true;relative=false;sync=true} @self
];
onEnd=[
  - time{mode=RESET;sync=true} @self
]} @self
```