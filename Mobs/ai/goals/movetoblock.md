Goal: Move To Block
--------------

Makes the mob move towards the specified block type. 

### 細項設定

| Attribute  | Aliases  | Description  | Default |
|----------------|----------|-----------------------------------------------|:-------:|
| material   |  | The block type to target  | |
| radius |  | The radius in which to search for the block   | |
| radiusy|  | The y radius in which to search for the block | |
| speed  |  | The speed of movement | |


### 範例

```yaml
ExampleMob:
  Type: Pig
  AIGoalSelectors:
- clear
- moveToBlock{material=STONE;radius=8;radiusY=2;speed=0.9}
```