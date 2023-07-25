## 用途
將靠近技能觸發半徑內的所有實體設為目標 相關技能:origin
這項目標選擇器是 **[EntitiesInRadius](/Skills/Targeters/EntitiesInRadius)** 的延伸, 可以直接使用, **他的相關細項設定**


## 細項設定
>*該目標器沒有獨立的細項設定，但可以使用 [EntitiesInRadius](/Skills/Targeters/EntitiesInRadius) 的相關細項設定*


## 範例
當創建的投射物由於某種原因結束時，他將傷害自身半徑 2 格內的所有生物
```yaml
  Skills:
  - projectile{...;
onTick=[
  - effect:particles @origin
];
onEnd=[
  - damage{a=10} @ENO{r=2}
]
} @target
```


## 簡化寫法
- [x] NearOrigin
- [x] ENO