用途
==============

讓目標發光，可以指定顏色

**需要插件 [GLOW API](https://www.spigotmc.org/resources/api-glowapi-1-9-1-10.19422/)**

細項設定
----------

| 設定項 | 簡化寫法 | 用途  | 預設值 |
|-----------|---------|---------------------------------|---------|
| color | c   | 顏色可以是: BLACK, DARK_BLUE, DARK_GREEN, DARK_AQUA, DARK_RED, DARK_PURPLE, GOLD, GRAY, DARK_GRAY, BLUE, GREEN, AQUA, RED, PURPLE, YELLOW, WHITE | white   |
| duration  | d   | 發光多久(單位:ticks)  | 100 |

範例
--------
```yaml
  Skills:
  - effect:glow{color=RED;duration=1000}
```