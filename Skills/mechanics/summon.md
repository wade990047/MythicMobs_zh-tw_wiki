## 用途

對目標召喚其他生物

## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| type  | t, mob, m| 要召喚的怪物   | SKELETON  |
| amount| a | 召喚怪物的數量   | 1   |
| level | l | 召喚的怪物等級 | 0   |
| radius| r, n| 在目標周圍半徑多少內生成 | 0   |
| yRadius   | yr, yn| 用來覆蓋垂直半徑| radius  |
| yRadiusUpOnly | yruo, yu| 是否讓垂直半徑只有上方| false   |
| velocity | v, f| 生物被召喚後的最大初始速度，使生物沿隨機平面方向前進  | 0   |
| yvelocity| yv, yf | 生物被召喚後的最大初始速度，使生物沿隨機垂直方向前進 | velocity|
| onSurface | os, s |是否只能生成在完整方塊上 | false   |
| copyThreatTable | ctt | 是否複製父級威脅表 | false   |
| inheritThreatTable | itt | 是否共用父級威脅表  | false   |
| inheritFaction | if   | 是否共用父級派系 | true|
| summonerIsOwner | sio | 召喚者是否為擁有者 | true|
| summonerIsParent | sip| 召喚者是否為父級| true|

  

## 範例

在半徑 20 格內的所有玩家身旁召喚 五隻凋零骷髏
```yml
RaiseSkeletons:
  Skills:
  - summon{type=WITHER_SKELETON;amount=5;radius=4} @PIR{r=20}
```