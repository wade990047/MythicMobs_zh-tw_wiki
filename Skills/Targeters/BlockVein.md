## Targeter: BlockVein
從技能的起點開始，將與方塊類型匹配的所有相鄰方塊設為目標

### 細項設定

| 設定項      | 簡寫         | 用途        | 預設值 |
|----------------|-----------------|--------------------------------------------------------|:-------:|
| blocktypes     | blocktype, bt, t, material, materials, mat, m, blocks, block, b | 方塊類型。可以是一個列表             | STONE   |
| limit          | max, l, m       | 添加到礦脈的方塊數量限制       | 10      |
| originMustMatch| match           | 目標方塊是否與技能起點處的方塊相匹配          | true    |

## 範例
```yaml
# 一次挖除周圍相同方塊
VeinMinerPickaxe:
  Id: NETHERITE_PICKAXE
  Skills:
  - breakblock{origin=@TargetBlock} @Vein{bt=<caster.raycast>} ~onBlockBreak

# 一次型挖除特定礦物
VeinMinerPickaxeOres:
  Id: DIAMOND_PICKAXE
  Skills:
  - breakblock{origin=@TargetBlock} @Vein{bt=REDSTONE_ORE, DEEPSLATE_REDSTONE_ORE} ~onBlockBreak

# 挖除所有礦物
VeinMinerPickaxeOres_V2:
  Id: DIAMOND_PICKAXE
  Skills:
  - breakblock{origin=@TargetBlock} @Vein{bt=#_ORE} ~onBlockBreak
```