## 用途
將施法者的前方設為目標


## 細項設定
| 設定項 | 簡寫   | 用途  | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| forward   | f, amount, a | 前方幾格  | 5   |
| rotate| rot   | 目標位置圍繞施法者的旋轉  | 0   |
| useeyelocation | uel  | 是否將視線位置用作目標選擇器的基礎  | false   |
| lockpitch |   | 是否鎖定傾角 | false   |


## 範例
```yaml
ExampleSkill:
  Skills:
  - effect:particles @Forward{f=3;uel=true;rot=10}
```