## 用途
裝備/移除目標實體馬鞍


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|----------------|-----------------|----------------------------------------------------|---------------|
| take   | t | 是否可以拿走馬鞍| false |


## 範例

```yml
ExampleSkill:
  Skills:
  - saddle{r=true} @self
```

##

製作一匹可以給自己配備臨時馬鞍的馬

```yml
ExampleMob:
  Type: HORSE
  Options:
    Tamed: true
  Skills:
  - aura{d=1200;auraName=TemporarySaddle;cd=600;sync=true;i=1;
  onStart=[
  - saddle @self
  ];
  onTick=[
  - e:p{p=crit;hs=0.3;vs=0.2;y=1;a=2} @self
  - closeinventory @Passenger
  ];
  onEnd=[
  - saddle{r=true} @self
  ]
  } @self ~onInteract
```