## 用途
Sets the target raider to patrol the given location


## 細項設定

| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| location  |block, l, b| A [Location Targeter], whose targeted location will be the specified one | |  


## 範例
```yml
  Skills:
  - setRaiderPatrolBlock{l=@TrackedLocation} @self
```

## 簡化寫法
- [x] setRaiderBlock

[Location Targeter]: /Skills/Targeters#single-location-targeters