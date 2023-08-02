## Mechanic: Saddle
Allows to either equip or remove a saddle on the target entity.


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|----------------|-----------------|----------------------------------------------------|---------------|
| take   | t | If the saddle should be taken away.| false |


## 範例

```yml
ExampleSkill:
  Skills:
  - saddle{r=true} @self
```

##

The following example is a bit more nuanced: it shows how a horse that can equip itself with a temporary saddle can be made
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