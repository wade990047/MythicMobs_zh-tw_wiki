# 目標選擇器

目標選擇器是用來決定技能使用後所要瞄準及應用的目標。

雖然目標選擇器在技術上是非必要設定的(默認目標選擇器是 `@trigger`)，但忘記設定目標選擇器是 MythicMobs 新手最常犯的錯誤之一。

當目標選擇器用於技能機制時，最外層技能內的所有技能都會繼承初始的目標選擇器。

但仍然可以通過為最外層技能內的各個技能提供自己的目標選擇器來覆蓋其主目標選擇器。

[[_TOC_]]

## 實體類目標選擇器

### 獨立實體目標選擇器

| 目標選擇器 | 其他寫法 | 用法|
|----------|-----------|---------------------------------------------------------------------------------|
| @[Self][]  | `@Caster` | 將自己設為技能目標 |
| @[Target][]  | `@T` | 技能使用者的目標  |
| @[Trigger][]  | | 將觸發技能的生物設為目標 |
| @[NearestPlayer][]  | | 將半徑內最近的玩家設為目標 |
| @[WolfOwner][]  | | 將狼的主人設為目標 |
| @[Owner][]  | | 將生物的擁有者設為目標 對應技能:**[owner](/skills/mechanics/setowner)** |
| @[Parent][]  | `@summoner`| 將生物的父母設為目標 對應技能:**[parent](/skills/mechanics/setparent)**|
| @[Mount][]  |  | 將目標正在騎乘的生物設為目標 |
| @[Children][]  | `@child`<br>`@summons`  | 將這隻生物所召喚的生物設為目標  |
| @[Father][]  | `@dad`| 將目標的父親設為目標  |
| @[Mother][]  | `@mom`  | 將目標的母親設為目標  |
| @[Passenger][]  | | 將正在騎乘自己的生物設為目標  |
| @[PlayerByName][]  | `@specificplayer`  | 將指定名稱的玩家設為目標，支援 Placeholder  |
| @[UniqueIdentifier][]  | `@UUID ` | 將指定UUID的生物設為目標，支援 Placeholder  |
| @[Vehicle][]  | | 將施術者的坐騎設為目標  |


### 複數實體目標選擇器

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|---------------------------------------------------------------------------------|
| @[LivingInCone][]  | `@livingEntitiesInCone`<br>`@EIC`| 將扇形範圍內的所有實體設為目標(可指定項:角度、半徑、旋轉角度)  |
| @[LivingInWorld][]| `@EIW`|將世界內的所有實體設為目標|
| @[NotLivingNearOrigin][]  |`@NLNO`| 將在指定半徑內的所有非生物實體設為目標 |
| @[PlayersInRadius][]  | `@PIR`  | 將半徑內的所有玩家設為目標  |
| @[MobsInRadius][]  | `@MIR`  | 將半徑內的所有指定怪物設為目標  |
| @[EntitiesInRadius][] | `@EIR`  | 將半徑內的所有實體設為目標 |
| @[EntitiesInRing][] | `@EIRR`  | 將指定環型中的所有實體設為目標 |
| @[PlayersInWorld][] | `@World` | 將當前世界的所有玩家設為目標 |
| @[PlayersOnServer][] | `@Server`<br>`@Everyone` | 將伺服器上的所有玩家設為目標 |
| @[PlayersInRing][] | | 將指定最小和最大半徑之間的所有玩家設為目標 |
| @[PlayersNearOrigin][] | | 將靠近技能觸發半徑內的所有玩家設為目標 相關技能:**[origin](/skills/targeters/origin)** |
| @[MobsNearOrigin][] | | 將靠近技能觸發半徑內的指定怪物設為目標 |
| @[EntitiesNearOrigin][]  | `@ENO`  | 將靠近技能觸發半徑內的所有實體設為目標 相關技能:**[origin](/skills/targeters/origin)**|
| @[Siblings][]  | `@sibling`  | 將與施法者擁有同一父母的任何生物設為目標 |
| @[ItemsNearOrigin][]  | | 將掉落在技能原始點附近的物品設為目標 **[origin](/skills/targeters/origin)** |
| @[ItemsInRadius][]  | `@IIR`  | 將半徑內的所有掉落物設為目標 |


### 威脅相關目標選擇器

要使用這些目標選擇器要確認 **[威脅表](/Mobs/ThreatTables)** 功能為啟用狀態.

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|---------------------------------------------------------------------------------|
| @[ThreatTable][]  | `@TT`  | 將存在於威寫表上的所有實體設為目標 |
| @[ThreatTablePlayers][]  | | 將在威脅表上的所有玩家設為目標  |
| @[RandomThreatTarget][]  | `@RTT`  | 將威脅表上的所有實體隨機選擇一個設為目標  |
| @[RandomThreatTargetLocation][]  | `@RTTL`  | 將威脅表上隨機實體的位置設為目標  |



## 位置目標選擇器

### 獨立位置目標選擇器

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|---------------------------------------------------------------------------------|
| @[SelfLocation][]  | `@casterLocation` | 將施法者的位置設為目標  |
| @[SelfEyeLocation][]  | `@eyeDirection`<br>`@casterEyeLocation`  | 將自身的所視位置設為目標  |
| @[Forward][]  || 將施法者的前方設為目標  |
| @[ProjectileForward][]  | | 將投射物前方相對於其方向的位置設為目標  |
| @[TargetLocation][]  | `@TL` | 將目標的位置設為目標|
| @[TriggerLocation][]  | | 將技能觸發者的位置設為目標  |
| @[SpawnLocation][]  | | 將世界重生點設為目標  |
| @[CasterSpawnLocation][]  | | 將施法者的重生點設為目標  |
| @[Location][]  | | 將世界的指定坐標設為目標  |
| @[Origin][]  | `@source`  | 將最外層技能的**起點**位置設為目標。通常會是施法生物，但在特殊情況下情況會是其他目標(例如投射物(Projectile)技能，其中**起點**是投射物的當前位置)|
| @[ObstructingBlock][]  | | 將施法者前方阻礙的方塊設為目標  |
| @[TrackedLocation][]  | | 將怪物正在追踪的位置設為目標  |
| @[NearestStructure][]  | | 將施法者世界半徑內最近的指定類型結構設為目標  |
| @[VariableLocation][]  | `@varLocation`  | 將指定變量(Variable)中存儲的位置設為目標  |


### 複數位置目標選擇器

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|---------------------------------------------------------------------------------|
| @[ForwardWall][]  | | 將施法者前方的平面位置設為目標  |
| @[PlayerLocationsInRadius][]  | `@PLIR`  | 將指定半徑內的所有玩家的位置設為目標 |
| @[Ring][]  | | 用點形成環型，將每點位置設為目標  |
| @[Cone][]  | | 將構成圓錐體的目標位置點設為目標 (注意：圓錐體固定在y軸上，不能上下旋轉)  |
| @[Sphere][]  | | 將施法者周圍球體中的點設為目標  |
| @[Rectangle][]  | `@cube`  | 將組成矩形的目標位置點設為目標  |
| @[RandomLocationsNearOrigin][]  | `@RLO`<br>`@RLNO`  | 將技能起點附近的隨機位置設為目標  |
| @[RingAroundOrigin][]  | `@RAO`  | 將定位原點周圍指定環型中的位置設為目標  |
| @[Spawners][]  | | 將指定刷怪籠的位置設為目標  |



## 繼承目標選擇器

下面的定位器稱為 **繼承目標選擇器** 他們的目標是相對於[繼承目標](Metaskills#inheritance)。例如：
```yaml
# Mob file
Laser:
  Type: CREEPER
  Display: 'Laser'
  Health: 12
  AITargetSelectors:
  - 0 clear
  - 1 players
  Skills:
  - skill{s=Laser} @target
```
```yaml
# Skill file
Laser:
  Skills:
  - ignite @EntitiesInLine{r=1}
```
在上面的示例技能中，`點燃(ignite)` 技能將瞄準施法者和 `- Skill{s=Laser} @target` 中指定的目標之間的所有實體，即施法者和目標之間的一條線。

一些主目標允許技能被`fromOrigin`施放。這會將主目標選擇器的起始位置更改為 `@Origin` 而不是施法者，這可以實現一些複雜的效果，特別是與投射物(Projectile)一起使用時。


### 繼承目標選擇器 實體配合

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|---------------------------------------------------------------------------------|
| @[LivingInLine][]  | `@LEIL`<br>`@EIL`  | 將繼承目標和施法生物之間一條線上的所有實體設為目標  |
| @[LivingNearTargetLocation][]  | `@LNTL`<br>`@ENT`  | 將繼承目標附近的所有實體設為目標  |
| @[PlayersNearTargetLocations][]  | `@PNTL`  | 將繼承目標附近的所有玩家設為目標  |
| @[TargetedTarget][]  | `@Targeted`  | 將繼承目標的實體設為目標  |


### 繼承目標選擇器 位置配合

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|---------------------------------------------------------------------------------|
| @[Line][]  | | 將生物和繼承目標之間的位置設為目標 |
| @[RandomLocationsNearTargets][]  | `@RLNT`<br>`@RLNTE`  | 將繼承目標周圍的隨機位置設為目標  |
| @[FloorOfTargets][]  | `@FOT`  | 將繼承目標的實體下方的方塊設為目標 |
| @[LocationsOfTargets][]  | `@LOT`  | 將繼承目標的實體位置設為目標|
| @[TargetedLocation][]  | `@targetedLoc`  | 將繼承目標位置的位置設為目標|
| @[BlocksInRadius][]  | `@BIR`  | 將繼承目標半徑內的所有方塊設為目標 |
| @[TargetBlock][]  | | 將玩家看著的方塊設為目標  |
| @[BlocksInChunk][]  | `@BIC`  | 將繼承目標的區塊中的所有方塊設為目標|
| @[BlocksNearOrigin][]  | `@BNO`  | 將主技能起點指定半徑內的所有方塊設為目標 |
| @[BlockVein][]  | `@vein`<br>`@bv`  | 從技能的起點開始，將與方塊類型匹配的所有相鄰方塊設為目標|


### 空 目標選擇器

| 目標選擇器 | 其他寫法 | 用法 |
|----------|-----------|------------------------------------------------------------------|
| @None | | 無目標 (對於沒有目標輸入的機制很有用) |



# 基本的細項設定
有一些通用屬性可以在大多數 目標選擇器(Targeter)中使用，具體取決於目標選擇器(Targeter)的返回值

## 可用於所有目標選擇器

### 強制指定細項設定
| 目標選擇器 | 其他寫法 | 用法 |
| ---------------------------------------- | ---------------- | ----------------------------------------- |
| sudoparent | parent  | 若這項設定被設置為 `true`, 目標選擇器將被設定為執行技能施法實體的 [Parent][] |
| sudoowner  | owner   | 若這項設定被設置為 `true`, 目標選擇器將被設定為執行技能施法實體的 [Owner][]  |
| sudotrigger| trigger | 若這項設定被設置為 `true`, 目標選擇器將被設定為執行技能施法實體的 [Trigger][]|

在下面這個範例中, [生物會不斷被傳送到其主人面前](https://cdn.discordapp.com/attachments/523443579574681600/1101186712174088253/a.gif)

因為目標選擇器`Forward`正在使用`sudoowner`的屬性，因此觸發後的目標會是執行技能的生物所有者
```yaml
TestOwner:
  Type: Wolf
  Skills:
  - setOwner @NearestPlayer{r=99} ~onSpawn
  - tp @Forward{f=5;y=1;sudoowner=true} ~onTimer:1
```


## 位置目標細項設定
| 目標選擇器 | 其他寫法 | 用法 |
| ---------------------------------------- | ---------------- | ----------------------------------------- |
| xoffset | xo, x  | 以起點為主的 **x** 軸偏移 |
| yoffset | yo, y  | 以起點為主的 **y** 軸偏移 |
| zoffset | zo, z  | 以起點為主的 **z** 軸偏移 |
| forwardOffset| foffset, fo | 以起點為主的 **前後** 偏移 以施術者視角為主|
| sideOffset | soffset, so | 以起點為主的 **左右** 偏移 以施術者視角為主|
| rotatex | rotx| 以起點為主的 **x** 軸旋轉|
| rotatey | roty| 以起點為主的 **y** 軸旋轉|
| rotatez | rotz| 以起點為主的 **z** 軸旋轉|
| coordinatex| cx| 設置 **x** 軸坐標|
| coordinatey| cy| 設置 **y** 軸坐標|
| coordinatez| cz| 設置 **z** 軸坐標|
| blocktypes | blocktype, bt| 僅針對指定的方塊類型，可以同時指定多個方塊，並用`,`分隔他們<br>可以在方塊類型前面添加`#`表示該方塊只需匹配類型中的部分內容，<br>添加`@`表示只需要匹配方塊類型的開頭 |
| blockignores | blockignore | 從目標選擇器中排除指定的方塊類型。可以通過使用`,`分隔來列出多個方塊 |
| coordinateyaw| cyaw| 設定偏移位置 |
| coordinatepitch | cpitch | 設置音高值 |
| blockcentered| centered | 布林值(true/false). 如果設定為 true, 目標位置的方塊中心將成為目標，而不是目標位置 |


# target-filters

## 目標篩選器

目標篩選器允許你篩選掉某些目標，並使目標選擇器更加靈活。

以下兩個設定項可擇一使用(可在任何目標選擇器上使用):

-ignore=X
-target=X

例如，要製作一個忽略所有玩家及動物的目標選擇器，你可以使用這個:

 damage{a=20} @EntitiesInRadius{r=10;ignore=players,animals}

例如，要製作一個只指定玩家的目標選擇器，你可以使用這個:

 skill{s=ASkill} @EntitiesInRadius{r=5;target=players}

可用的篩選器選項:

-self **自己**

-animals **友善生物**

-armorstands/armor_stands **盔甲座**

-creative *(預設為忽略狀態)* **創造模式**

-creatures  **生物**

-flyingmobs **盔甲座**

-marker

-monsters **敵對生物**

-NPCs *(Citizens NPCs 預設為忽略狀態)* **NPC**

-players **玩家**

-samefaction **相同派系**

-spectators *(預設為忽略狀態)* **觀察者模式**

-vanilla 

-villager **村民**

-watermobs **水下生物**

-owner **擁有者**


你可以通過添加選項來關閉特定過濾器
**targetXXXXX** 將 XXXXX 替換為過濾器名稱，例如
**targetPlayers=false** 或 **targetcreative=true**

注意：從 MM 4.15 或 MM 5.0 開始，您可以在 MythicMobs/config.yml 中設置默認目標篩選器

## 目標選擇器限制

所有實體和位置定位器還支持目標限制（從 v5.0.4 開始）。通過此功能，你可以限制目標實體/位置的數量，包括選擇它們的順序.

可以通過以下設定項完成：

-limit=# **最大上限**
-sort=X **排序方式**

假設你要將半徑內 30 格方塊內最近的 2 個玩家設為目標。為此，你需要將最大上限設置為 2 並按最接近的距離排序：

-**@PlayersInRadius{r=30;limit=2;sort=NEAREST}**

目前，排序方式可以有以下方式:

**距離排序選擇器**
- NONE **按目標存在的時間排序**
- RANDOM **隨機選擇目標**
- NEAREST **距離越近的目標**
- FURTHEST **距離越遠的目標**

**實體排序選擇器**
- HIGHEST_HEALTH **血量越高的目標**
- LOWEST_HEALTH **血量越低的目標**
- HIGHEST_THREAT **威脅值越高的目標**
- LOWEST_THREAT **威脅值越低的目標**


<!-- LINKS -->
<!-- Single Entity Targeters -->
  [Children]: /Skills/Targeters/Children
  [Father]: /Skills/Targeters/Father
  [Mother]: /Skills/Targeters/Mother
  [Mount]: /Skills/Targeters/Mount
  [NearestPlayer]: /Skills/Targeters/NearestPlayer
  [Owner]: /Skills/Targeters/Owner
  [Parent]: /Skills/Targeters/Parent
  [Passenger]: /Skills/Targeters/Passenger
  [PlayerByName]: /Skills/Targeters/PlayerByName
  [Self]: /Skills/Targeters/Self
  [Target]: /Skills/Targeters/Target
  [Trigger]: /Skills/Targeters/Trigger
  [UniqueIdentifier]: /Skills/Targeters/UniqueIdentifier
  [Vehicle]: /Skills/Targeters/Vehicle
  [WolfOwner]: /Skills/Targeters/WolfOwner
<!-- Multi Entity Targeters -->
  [EntitiesInRadius]: /Skills/Targeters/EntitiesInRadius
  [EntitiesInRing]: /Skills/Targeters/EntitiesInRing
  [EntitiesNearOrigin]: /Skills/Targeters/EntitiesNearOrigin
  [ItemsInRadius]: /Skills/Targeters/ItemsInRadius
  [ItemsNearOrigin]: /Skills/Targeters/ItemsNearOrigin
  [LivingInCone]: /Skills/Targeters/LivingInCone
  [LivingInWorld]: /Skills/Targeters/LivingInWorld
  [MobsInRadius]: /Skills/Targeters/MobsInRadius
  [MobsNearOrigin]: /Skills/Targeters/MobsNearOrigin
  [NotLivingNearOrigin]: /Skills/Targeters/NotLivingNearOrigin
  [PlayerLocationsInRadius]: /Skills/Targeters/PlayerLocationsInRadius
  [PlayersInRadius]: /Skills/Targeters/PlayersInRadius
  [PlayersInRing]: /Skills/Targeters/PlayersInRing
  [PlayersInWorld]: /Skills/Targeters/PlayersInWorld
  [PlayersNearOrigin]: /Skills/Targeters/PlayersNearOrigin
  [PlayersOnServer]: /Skills/Targeters/PlayersOnServer
  [Siblings]: /Skills/Targeters/Siblings
<!-- ThreatTable Targeters -->
  [ThreatTable]: /Skills/Targeters/ThreatTable
  [ThreatTablePlayers]: /Skills/Targeters/ThreatTablePlayers
  [RandomThreatTarget]: /Skills/Targeters/RandomThreatTarget
  [RandomThreatTargetLocation]: /Skills/Targeters/RandomThreatTargetLocation
<!-- Single Location Targeters -->
  [CasterSpawnLocation]: /Skills/Targeters/CasterSpawnLocation
  [Forward]: /Skills/Targeters/Forward
  [Location]: /Skills/Targeters/Location
  [NearestStructure]: /Skills/Targeters/NearestStructure
  [ObstructingBlock]: /Skills/Targeters/ObstructingBlock
  [Origin]: /Skills/Targeters/Origin
  [ProjectileForward]: /Skills/Targeters/ProjectileForward
  [SelfEyeLocation]: /Skills/Targeters/SelfEyeLocation
  [SelfLocation]: /Skills/Targeters/SelfLocation
  [SpawnLocation]: /Skills/Targeters/SpawnLocation
  [VariableLocation]: /Skills/Targeters/VariableLocation
  [TargetBlock]: /Skills/Targeters/TargetBlock
  [TargetLocation]: /Skills/Targeters/TargetLocation
  [TrackedLocation]: /Skills/Targeters/TrackedLocation
  [TriggerLocation]: /Skills/Targeters/TriggerLocation
<!-- Multi Location Targeters -->
  [Cone]: /Skills/Targeters/Cone
  [ForwardWall]: /Skills/Targeters/ForwardWall
  [RandomLocationsNearOrigin]: /Skills/Targeters/RandomLocationsNearOrigin
  [RandomLocationsNearCaster]: /Skills/Targeters/RandomLocationsNearCaster
  [Rectangle]: /Skills/Targeters/Rectangle
  [RingAroundOrigin]: /Skills/Targeters/RingAroundOrigin
  [Ring]: /Skills/Targeters/Ring
  [Spawners]: /Skills/Targeters/Spawners
  [Sphere]: /Skills/Targeters/Sphere
<!-- Meta Targeters -->
  [BlocksInRadius]: /Skills/Targeters/BlocksInRadius
  [BlocksInChunk]: /Skills/Targeters/BlocksInChunk
  [BlocksNearOrigin]: /Skills/Targeters/BlocksNearOrigin
  [BlockVein]: /Skills/Targeters/BlockVein
  [FloorOfTargets]: /Skills/Targeters/FloorOfTargets
  [Line]: /Skills/Targeters/Line
  [LivingInLine]: /Skills/Targeters/LivingInLine
  [LivingNearTargetLocation]: /Skills/Targeters/LivingNearTargetLocation
  [LocationsOfTargets]: /Skills/Targeters/LocationsOfTargets
  [PlayersNearTargetLocations]: /Skills/Targeters/PlayersNearTargetLocations
  [RandomLocationsNearTargets]: /Skills/Targeters/RandomLocationsNearTargets
  [TargetedLocation]: /Skills/Targeters/TargetedLocation
  [TargetedTarget]: /Skills/Targeters/TargetedTarget