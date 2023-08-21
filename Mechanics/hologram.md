用途
================
在目標位置設置一個漂浮文字

細項設定
---------------

| 設定項 | 簡化寫法 | 用途 | 預設值 |
| ---------- | ----- | ---------------- | ----- |
|text| t | 要顯示的文字 | Hologram Text Missing |
|stay| time  | 要顯示多久(單位:ticks) | 100 |

範例
-----------
當怪物被右鍵互動時，在自己的位置高1.6格的地方召喚漂浮文字
```yaml
Skills:
- holo{text="Example Text";time=100} @selflocation{y=1.6} ~onInteract
```
- [x] 簡化寫法: summonhologram, holo