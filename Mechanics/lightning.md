用途
===================

對目標打雷，並造成傷害及燃燒(僅在有開啟火焰延燒的情況下發生)

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|--------------------------------------------|---------------|
| damage| d   | 閃電給予目標的傷害. | 0.01337   |

  

範例
--------

對半徑10格內的所有實體劈下一道閃電。

```yaml
StaticSheep:
  Type: SHEEP
  Skills:
  - lightning @EntitiesInRadius{r=10} ~onTimer:100
```
對半徑10格內的所有實體劈下一道閃電，並造成6點傷害。

```yaml
StaticSheep:
  Type: SHEEP
  Skills:
  - lightning{d=6} @EntitiesInRadius{r=10} ~onTimer:100
```