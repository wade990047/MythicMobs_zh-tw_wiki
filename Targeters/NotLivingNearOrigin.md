## 用途
將在指定半徑內的所有非生物實體設為目標


## 細項設定
| 設定項 | 簡寫   | 用途                      | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| radius    | r         | 目標半徑範圍       | 5       |


## 範例
技能一旦結束，該技能將在聊天室中說出離自己半徑 10 格內的每個非生物實體的 UUID
```yaml
ExampleSkill:
  Skills:
  - projectile{...;
    onEnd=[
      - command{c="say <target.uuid>"} @NotLivingNearOrigin{r=10}
    ]}
```

## 簡化寫法
- [x] nonLivingNearOrigin
- [x] NLNO