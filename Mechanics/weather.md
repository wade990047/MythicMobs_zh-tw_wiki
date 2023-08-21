用途
=================

更改世界天氣

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|-----------------------------------------------------------|---------|
| type  | sunny | 天氣類型可以是 "sunny", "rainy", 或 "stormy" | sunny   |
| duration  |   | 持續時間(單位:ticks)| 500 |

  
天氣類型/簡化:  
|天氣類型|簡化寫法|
|------------|----------------|
|**Sunny**| sun, clear|
| **Rainy**  | rain   |
| **Stormy** | storm, thunder |

範例
--------

```yml
  Skills:
  - weather{type=storm;duration=6000} ~onSpawn
```