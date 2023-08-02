用途
=====================

射出凋零骷髏頭顱

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|---------|---------------------------------------------------------------------|---------------|
| yield | y   | 爆炸威力 | 1 |
| playsound | ps  | 是否播放聲音 | false |

  

範例
--------

```yml
SkullBarrage:
  Skills:
  - shootskull{y=1;v=4} @target
  - delay 10
  - shootskull{y=1;v=4} @target
  - delay 10
  - shootskull{y=1;v=4} @target
```