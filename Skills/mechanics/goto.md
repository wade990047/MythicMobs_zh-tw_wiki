用途
============================

向目標位置(實體或位置)移動

細項設定
----------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|---------------|---------|----------------|---------------|
| speedModifier | s   | 移動速度倍率  | 1 |
| spreadH   | sh  | 水平移動速度 | 0 |
| spreadV   | sv  | 垂直移動速度   | 0 |

範例
--------
```yml
Skills:
  - goto{speedModifier=1;sh=5;sv=5} @owner
  - goto{speedModifier=1;sh=5;sv=5} @location{c=100,65,100}
```
