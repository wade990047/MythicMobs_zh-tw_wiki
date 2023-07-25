技能機制
===============

技能機制(基本技能)是內建的技能基礎，你可以在你的怪物中單獨調用這些基本技能。

你可以通過組合這些基本技能來創建自己的技能組合。

有些技能能夠將實體、位置設為目標，有些不能設定任何目標。你可以用[目標選擇器][]控制你的技能目標

了解 MM v4.12 中新添加的技能參數系統 [這裡!][]

基本技能
---------

這些技能通常針對實體（玩家或其他生物），但有些技能也能夠將位置設為目標。

| 技能名稱  | 用途|
|---------------------------|----------------------------------------------------------------------------|
| [ActivateSpawner][]   | 在目標位置激活 MythicMobs 刷怪籠 |
| [AddTrade][]  | 改變村民的交易內容|
| [AnimateArmorStand][] | 設定盔甲座動畫 |
| [ArrowVolley][]   | 同時發射許多箭矢   |
| [Attribute][] | 設置目標實體的屬性(如果含有可設定項)   |
| [AttributeModifier][] | 向可設定屬性的目標添加屬性倍率器  |
| [AuraRemove][]| 移除指定目標的光環(Aura)  |
| [BarCreate][] | 在施法生物上創建一個自定義BOSS血條|
| [BarRemove][] | 在施法生物上移除一個自定義BOSS血條   |
| [BarSet][]| 在施法生物上編輯一個自定義BOSS血條|
| [BlockDestabilize][]  | 使目標方塊掉落(方塊類型需受重力影響)|
| [BlockPhysics][]  | 在目標位置觸發方塊更新 |
| [BoneMeal][]  | 對目標方塊使用骨粉 |
| [BossBorder][]| 在生物周圍創建一個無法逃脫的結界   |
| [BreakBlock][]| 破壞目標位置的方塊 |
| [BreakBlockAndGiveItem][] | 破壞目標位置的方塊並掉落指定物品|
| [ClearExperienceLevels][] | 清除目標玩家經驗等級   |
| [GiveExperienceLevels][]  | 給予目標玩家經驗等級   |
| [TakeExperienceLevels][]  | 減少目標玩家經驗等級|
| [CloseInventory][]| 關閉目標玩家的物品欄|
| [Command][]   | 讓目標執行指令  |
| [Consume][]   | 擊中目標後造成傷害並恢復自身生命值|
| [ConsumeSlot][]   | 從玩家物品欄的特定位置移除物品|
| [Disengage][] | 使施法者向後跳躍遠離目標實體  |
| [Disguise][]  | 改變施法者的偽裝樣貌  |
| [DisguiseModify][]| 修改施法者已經應用的偽裝樣貌  |
| [DisguiseTarget][]| 改變目標的偽裝樣貌  |
| [Undisguise][]| 移除施法者的偽裝樣貌   |
| [Dismount][]  | 使施法者取消騎乘，無論他們騎著什麼   |
| [DisplayTransformation][] | 設置目標顯示的轉換同型實體  |
| [ClearThreat][]   | 清除怪物威脅表  |
| [CurrencyGive][]  | 給予玩家金錢. 需要 Vault 及經濟配合插件|
| [CurrencyTake][]  | 拿走玩家金錢. 需要 Vault 及經濟配合插件   |
| [Damage][]| 對目標造成傷害|
| [BaseDamage][]| 以怪物的傷害為基礎，造成指定倍率的傷害   |
| [DamagePercent][] | 以目標的當前血量為基礎，造成指定比例的傷害   |
| [Decapitate][]| 掉落目標頭顱|
| [Doppleganger][]  | 複製目標玩家的樣貌  |
| [DropItem][]  | 在目標位置掉落指定物品   |
| [EjectPassenger][]| 將任何騎在自己身上的實體給甩下  |
| [Equip][] | 讓施術者裝備指定物品|
| [Explosion][] | 爆炸|
| [Extinguish][]| 將生物的燃燒狀態移除   |
| [FawePaste][] | 貼上 FAWE 的選取建築 (插件:Fast Async World Edit)   |
| [Feed][]  | 回復目標玩家飽食度|
| [FillChest][] | 將箱子填充指定物品|
| [Fly][]   | 施加[光環][]，使目標玩家能夠飛行  |
| [ForcePull][] | 將目標傳送至施法者 |
| [Freeze][]| 對目標使用粉雪凍結效果並凍結指定的時間 |
| [Glow][]  | 讓目標發光 |
| [GiveItem][]  | 給予目標指定物品|
| [GiveItemFromSlot][]  | 給予目標施法者指定欄位的物品   |
| [GoTo][]  | 向目標位置(實體或位置)移動   |
| [Heal][]  | 回復目標血量   |
| [HealPercent][]   | 以最大血量為基礎的比例回復目標血量|
| [Hide][]  | 時間內對目標玩家隱藏施法者 |
| [Hologram][]  | 在目標位置設置一個漂浮文字 |
| [Ignite][]| 點燃目標|
| [JSONMessage][]   | 對目標玩家送出一則 JSON 格式的訊息 |
| [Jump][]  | 讓施法者向上跳  |
| [Leap][]  | 讓施法者向前衝刺|
| [Lightning][] | 對目標打雷|
| [Look][]  | 讓施法者看著目標 |
| [Lunge][] | 使施法者向前沖向目標   |
| [Message][]   | 對目標玩家發送訊息|
| [ModifyGlobalScore][] | 修改全域的記分版值： \_\_GLOBAL\_\_   |
| [ModifyTargetScore][] | 修改玩家的記分板值   |
| [ModifyMobScore][]| 修改怪物的記分板值  |
| [ModifyScore][]   | 修改Dummy的記分板值|
| [Mount][] | 為施法者生成一隻生物並騎上他 |
| [MountMe][]   | 強制目標生物騎上自己  |
| [MountTarget][]   | 騎上目標  |
| [Oxygen][]| 幫目標玩家補充氧氣|
| [PickUpItem][]| 撿起目標物品  |
| [PlayBlockBreakSound][]   | 播放方塊破壞的聲音   |
| [PlayBlockFallSound][]| 播放方塊墜落的聲音|
| [PlayBlockHitSound][] | 播放跌落方塊的聲音|
| [PlayBlockPlaceSound][]   | 播放放置方塊的聲音  |
| [PlayBlockStepSound][]| 播放踩上方塊的聲音   |
| [PoseArmorStand][]| 設定盔甲座的姿勢   |
| [Potion][]| 給予目標藥水效果   |
| [PotionClear][]   | 清除目標藥水效果  |
| [Prison][]| 將目標囚禁在方塊內 |
| [Propel][]| 將施法者推向目標|
| [Pull][]  | 將目標拉向生物|
| [PushButton][]| 在目標位置按下按鈕  |
| [RayTrace][]  | 沿著直線到達目標|
| [Rally][] | 使附近的其他生物一起攻擊目標   |
| [RandomMessage][] | 對目標玩家發送隨機訊息 |
| [Remount][]   | 重新騎乘施法者最初騎乘的生物(如果它還活著)  |
| [Remove][]| 移除目標生物 |
| [RemoveHeldItem][]| 移除玩家手上的物品  |
| [RemoveOwner][]   | 移除生物的擁有者資料 |
| [RunAIGoalSelector][] | 執行目標的 AIGoalSelectors |
| [RunAITargetSelector][]   | 執行目標的 AITargetSelectors   |
| [Saddle][]| 裝備/移除目標實體馬鞍|
| [SendActionMessage][] | 對目標玩家送出提示欄訊息|
| [SendResourcePack][]  | 對目標玩家送出材質包更新 |
| [SendTitleMessage][]  | 對目標玩家送出標題與副標題訊息|
| [SendToast][] | 對目標玩家送出成就框訊息 |
| [SetAI][] | 關閉/啟用 目標生物的AI   |
| [SetBlockType][]  | 更改目標位置的方塊類型   |
| [SetCollidable][] | 設置目標是否應該有可碰撞的碰撞箱|
| [SetDragonPodium][]   | 將終界龍的平台位置設置在目標位置|
| [SetGameMode][]   | 設置目標玩家的遊戲模式 |
| [SetGliding][]| 如果目標有鞘翅，則使目標滑翔  |
| [SetGlobalScore][]| 設置全域記分板分數: \_\_GLOBAL\_\_  |
| [SetGravity][]| 設置重力是否影響目標實體  |
| [SetHealth][] | 設置目標實體的血量   |
| [SetLeashHolder][]| 更改栓繩的持有者|
| [SetLevel][]  | 更改施法者的生物等級|
| [SetMaterialCooldown][]   | 設定可使用物品的冷卻時間 如:終界珍珠、歌萊果等等|
| [SetMaxHealth][]  | 設置目標實體的最大血量|
| [SetMobColor][]   | 設置生物的顯示顏色(如果可變更顏色)|
| [SetMobScore][]   | 設置施法者生物的記分板分數  |
| [SetName][]   | 改變目標實體的名稱|
| [SetRaiderPatrolBlock][]  | 設置突襲者的巡邏位置   |
| [SetRaiderPatrolLeader][] | 設定目標為突襲的隊長   |
| [SetFaction][]| 改變目標實體的派系   |
| [SetNoDamageTicks][]  | 設置目標的 NoDamageTicks|
| [SetOwner][]  | 設定目標為施法者的擁有者   |
| [SetParent][] | 設定目標為施法者的父母 |
| [SetProjectileDirection][]| 設定投射物的方向   |
| [SetProjectileBulletModel][]| 設定投射物的子彈模型. (只會顯示子彈)|
| [SetRotation][]   | 設定目標的轉向|
| [SetTarget][] | 設定目標  |
| [SetTargetScore][]| 設定目標的記分板分數   |
| [SetTongueTarget][]   | 將青蛙的舌頭目標設置為目標|
| [SetScore][]  | 設定 Dummy 的記分板分數 |
| [SetSpeed][]  | 設定目標實體的移動速度   |
| [SetStance][] | 設置目標生物的姿態   |
| [Shield][]| 對目標實體新增吸收傷害血量   |
| [ShieldBreak][]   | 強制玩家取消護盾狀態並使其進入冷卻狀態  |
| [ShieldPercent][] | 對目標實體新增以最大血量為基礎，取比例的吸收傷害血量   |
| [ShootFireball][] | 射出燃燒彈|
| [ShootPotion][]   | 丟出藥水  |
| [ShootSkull][]| 射出凋零骷髏頭顱 |
| [ShootShulkerBullet][]| 設出界伏蚌的子彈   |
| [ShowEntity][]| 顯示對目標玩家隱形的實體|
| [Signal][]| 對目標怪物發送信號|
| [Speak][] | 使怪物在聊天中說話，並提供語言氣泡的選項   |
| [Spring][]| 在目標位置產生臨時液體  |
| [Stun][]  | 使目標實體暈眩|
| [StopUsingItem][] | 停止目標實體正在使用的物品|
| [Suicide][]   | 使施法者死亡   |
| [Summon][]| 對目標召喚其他生物   |
| [SummonPassenger][]   | 召喚生物騎在目標身上|
| [Swap][]  | 和目標交換位置|
| [AddTag][]| 對目標新增一個記分板標籤|
| [RemoveTag][] | 對目標移除一個記分板標籤   |
| [TakeItem][]  | 從目標玩家的物品欄中移除物品   |
| [Teleport][]  | 傳送到目標|
| [TeleportY][] | 傳送到目標的垂直位置   |
| [TeleportIn][]| 相對於施法者的偏移量傳送目標  |
| [TeleportTo][]| 傳送目標到指定位置   |
| [Time][]  | 更改世界時間  |
| [Threat][]| 編輯目標對於施法者威脅表的威脅值|
| [Throw][] | 將目標實體向外丟   |
| [ToggleLever][]   | 在指定位置拉下拉桿  |
| [ToggleSitting][] | 使生物坐下(需有可坐下的設定項)   |
| [TrackLocation][] | 將生物的追隨位置設置為目標位置|
| [UndoPaste][] | 復原上一個貼上的動作 |
| [Velocity][]  | 編輯目標實體的重力  |
| [Weather][]   | 更改世界天氣   |
| [WolfSit][]   | 強制使狼坐下 |

特效技能
----------------

特效技能可為你的技能添加特效。

[在這裡查看所有可用特效][]

高級/特殊技能
-----------------------

這些技能機制具有特殊的高級功能，並且大多數用於調用其他技能。

如果您指定一個目標，則所有其他技能都將 **繼承** 目標(在適用的條件下)。

| 技能名稱| 用途 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **[Skill][]**   | 技能組   |
| **[VariableSkill][]**   | 變數技能組，可使用佔位符(Placeholder) 作為技能名稱  |
| [Aura][]| 將光環應用於目標實體，允許在 ***onStart/onTick/onEnd*** 上運行所有源自目標的技能 |
| [CancelEvent][] | 取消觸發當前技能組的事件，僅適用於某些觸發器  |
| [Cast][]| 使用各種特殊設定來 **施放** 技能 |
| [Chain][]   | 在多個目標之間形成鎖鏈並施放技能|
| [ChainMissile][]| 在實體之間形成鎖鏈的導彈. **付費版限定技能** |
| [Delay][]   | 與下一個技能之間延遲多少ticks  |
| [EndProjectile][]   | 強制停止投射物 只適用於射彈(Projectile)|
| [GlobalCooldown][]  | 設置施法者的全域冷卻  |
| [Missile][] | 向目標發射一枚自導砲彈|
| [ModifyProjectile][]| 編輯射彈類技能 projectile / missile / orbital |
| [OnAttack][]| 對目標施加[光環][]，攻擊時觸發技能  |
| [OnDamaged][]   | 對目標施加[光環][]，受傷時觸發技能 |
| [OnShoot][] | 對目標施加[光環][]，射弓時觸發技能  |
| [OnBlockBreak][]| 對目標施加[光環][]，破壞方塊時觸發技能|
| [OnBlockPlace][]| 對目標施加[光環][]，放置方塊時觸發技能|
| [OnSwing][] | 對目標施加[光環][]，左鍵/揮劍時觸發技能   |
| [OnInteract][]  | 對目標施加[光環][]，右鍵/互動時觸發技能(對空氣無效) |
| [OnJump][]  | 對目標施加[光環][]，跳躍時觸發技能 (伺服器端限定為 PAPER)  |
| [OnDeath][] | 對目標施加[光環][]，死亡時觸發技能 |
| [Orbital][] | 對目標施加[光環][]，讓射彈(Projectile)環繞在玩家周圍 |
| [Polygon][] | 創建一個可以執行技能的自定義多邊形圖案   |
| [Projectile][]  | 射出自定義的投射物|
| [ProjectileVelocity][]  | 修改 射彈(Projectile)或導彈(Missle)的速度|
| [RandomSkill][] | 隨機執行列表中的技能 |
| [SetSkillCooldown][]| 設定技能冷卻(單位:秒)|
| [Shoot][]   | 對目標射出物品投射物 如:箭矢/雞蛋/雪球 |
| [Slash][]   | 創建可以執行技能的自定義斜線圖形 |
| [SudoSkill][]   | 讓目標強制執行技能|
| [Switch-Case][] | 讓執行技能的方式向 switch/case 一樣 |
| [Totem][]   | 在目標位置創建一個可執行技能的靜態 **圖騰**  |
| [Volley][]  | 使用多個選項向目標發射一連串射彈(Projectile)  |
| [VariableAdd][] | 將指定變量添加數值|
| [VariableMath][]| 讓指定變量進行數學運算 |
| [SetVariable][] | 將指定變量設定數值|
| [SetVariableLocation][] | 將指定變量設置位置   |
| [VariableUnset][]   | 將指定變量刪除 |
| [VariableSubtract][]| 將指定變量減少數值  |

全域細項設定
--------------------

下方的細項設定可適用於所有技能

| 設定名稱 | 簡化寫法   | 用途| 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| cooldown  | cd| 技能冷卻時間(單位:秒)  | 0   |
| delay |   | 技能距上一技能的延遲時間(單位:ticks)   | 0   |
| repeat|   | 技能應該要重複執行幾次   | 0   |
| repeatInterval | repeatI | 技能每次重複執行應該要間格多久(單位:ticks)| 0   |
| targetInterval | targetI | 目標重新選擇之間必須要間格多久(單位:ticks)   | 0   |
| origin  ||將起點更改為提供的任何目標器. `origin=@Forward{f=10}` **付費版限定**|   |
| forcesync | sync  | 強制執行類型為 SYNC| false   |
| power |   | [Power](/mobs/Power) 倍率 | 1   |
| fromorigin | fo   | 是否從起點執行技能| false   |
| targetisorigin |  | 是否將目標設為起點   | false   |
| targetcreative |  | 是否把創造模式的玩家設為目標 | false   |
| splitPower | powersplit | 是否在各目標間將力量分散 | false |

<!--
Upcoming Mechanics
------------------

These mechanics are currently being worked on and will be in future
releases of the plugin. Some mechanics listed here are already included,
but not yet ready for use.

| Mechanic   | Description |
|--------------------|---------------------------------|
-->

  [這裡!]: /skills/skillparametersystem
  [目標選擇器]: /skills/targeters/
  [ActivateSpawner]: /skills/mechanics/activatespawner
  [AddTrade]: /skills/mechanics/AddTrade
  [AnimateArmorStand]: /skills/mechanics/animatearmorstand
  [ArrowVolley]: /skills/mechanics/arrowvolley
  [Attribute]: /skills/mechanics/Attribute
  [AttributeModifier]: /skills/mechanics/AttributeModifier
  [AuraRemove]: /skills/mechanics/auraremove
  [BarCreate]: /skills/mechanics/barcreate
  [BarSet]: /skills/mechanics/barset
  [BarRemove]: /skills/mechanics/barremove
  [BlockDestabilize]: /skills/mechanics/blockdestabilize
  [BlockPhysics]: /skills/mechanics/blockphysics
  [BoneMeal]: /skills/mechanics/bonemeal
  [BossBorder]: /skills/mechanics/bossborder
  [BreakBlock]: /skills/mechanics/breakblock
  [BreakBlockAndGiveItem]: /skills/mechanics/breakBlockAndGiveItem
  [ClearExperienceLevels]: /skills/mechanics/ClearExperienceLevels
  [GiveExperienceLevels]: /skills/mechanics/GiveExperienceLevels
  [TakeExperienceLevels]: /skills/mechanics/TakeExperienceLevels
  [CloseInventory]: /skills/mechanics/closeinventory
  [Command]: /skills/mechanics/command
  [Consume]: /skills/mechanics/consume
  [ConsumeSlot]: /skills/mechanics/consumeslot
  [Disengage]: /skills/mechanics/disengage
  [Disguise]: /skills/mechanics/disguise
  [DisguiseModify]: /skills/mechanics/DisguiseModify
  [DisguiseTarget]: /skills/mechanics/disguisetarget
  [Undisguise]: /skills/mechanics/undisguise
  [Dismount]: /skills/mechanics/dismount
  [DisplayTransformation]: /skills/mechanics/DisplayTransformation
  [ClearThreat]: /skills/mechanics/clearthreat
  [CurrencyGive]: /skills/mechanics/currencygive
  [CurrencyTake]: /skills/mechanics/currencytake
  [Damage]: /skills/mechanics/damage
  [BaseDamage]: /skills/mechanics/basedamage
  [DamagePercent]: /skills/mechanics/percentdamage
  [Decapitate]: /skills/mechanics/decapitate
  [Doppleganger]: /skills/mechanics/doppleganger
  [DropItem]: /skills/mechanics/dropitem
  [EjectPassenger]: /skills/mechanics/ejectpassenger
  [Equip]: /skills/mechanics/equip
  [Explosion]: /skills/mechanics/explosion
  [Extinguish]: /skills/mechanics/extinguish
  [FawePaste]: /skills/mechanics/fawepaste
  [Feed]: /skills/mechanics/feed
  [FillChest]: /skills/mechanics/fillChest
  [Fly]: /skills/mechanics/fly
  [Freeze]: /skills/mechanics/freeze
  [光環]: /skills/mechanics/aura
  [ForcePull]: /skills/mechanics/forcepull
  [Glow]: /skills/mechanics/glow
  [GiveItem]: /skills/mechanics/giveitem
  [GiveItemFromTarget]: /skills/mechanics/giveitemfromtarget
  [GoTo]: /skills/mechanics/goto
  [Heal]: /skills/mechanics/heal
  [HealPercent]: /skills/mechanics/healpercent
  [Hologram]: /skills/mechanics/hologram
  [Ignite]: /skills/mechanics/ignite
  [JSONMessage]: /skills/mechanics/jsonmessage
  [Jump]: /skills/mechanics/jump
  [Leap]: /skills/mechanics/leap
  [Lightning]: /skills/mechanics/lightning
  [Look]: /skills/mechanics/look
  [Lunge]: /skills/mechanics/lunge
  [Message]: /skills/mechanics/message
  [ModifyGlobalScore]: /skills/mechanics/modifyglobalscore
  [ModifyTargetScore]: /skills/mechanics/modifytargetscore
  [ModifyMobScore]: /skills/mechanics/modifymobscore
  [ModifyScore]: /skills/mechanics/modifyscore
  [Mount]: /skills/mechanics/mount
  [MountMe]: /skills/mechanics/mountme
  [MountTarget]: /skills/mechanics/mounttarget
  [Oxygen]: /skills/mechanics/oxygen
  [PickUpItem]: /skills/mechanics/pickupitem
  [PoseArmorStand]: /skills/mechanics/posearmorstand
  [Potion]: /skills/mechanics/potion
  [PotionClear]: /skills/mechanics/potionclear
  [Prison]: /skills/mechanics/prison
  [Propel]: /skills/mechanics/propel
  [Pull]: /skills/mechanics/pull
  [PushButton]: /skills/mechanics/pushbutton
  [Rally]: /skills/mechanics/rally
  [RandomMessage]: /skills/mechanics/randommessage
  [RayTrace]: /skills/mechanics/raytrace
  [Remount]: /skills/mechanics/remount
  [Remove]: /skills/mechanics/remove
  [RemoveHeldItem]: /skills/mechanics/removehelditem
  [RemoveOwner]: /skills/mechanics/removeowner
  [RunAIGoalSelector]: /skills/mechanics/runaigoalselector
  [RunAITargetSelector]: /skills/mechanics/runaitargetselector
  [Saddle]: /skills/mechanics/saddle
  [SendActionMessage]: /skills/mechanics/sendactionmessage
  [SendResourcePack]: /skills/mechanics/sendresourcepack
  [SendTitleMessage]: /skills/mechanics/sendtitlemessage
  [SendToast]: /skills/mechanics/sendtoast
  [SetAI]: /skills/mechanics/setai
  [SetBlockType]: /skills/mechanics/setblocktype
  [SetCollidable]: /skills/mechanics/setcollidable
  [SetDragonPodium]: /skills/mechanics/SetDragonPodium
  [SetGameMode]: /skills/mechanics/setgamemode
  [SetGliding]: /skills/mechanics/setgliding
  [SetGlobalScore]: /skills/mechanics/setglobalscore
  [SetGravity]: /skills/mechanics/setgravity
  [SetHealth]: /skills/mechanics/sethealth
  [SetLeashHolder]: /skills/mechanics/setleashholder
  [SetLevel]: /skills/mechanics/setlevel
  [SetMaterialCooldown]: /skills/mechanics/setmaterialcooldown
  [SetMaxHealth]: /skills/mechanics/setmaxhealth
  [SetMobColor]: /skills/mechanics/setmobcolor
  [SetMobScore]: /skills/mechanics/setmobscore
  [SetName]: /skills/mechanics/setname
  [SetNoDamageTicks]: /skills/mechanics/setnodamageticks
  [SetOwner]: /skills/mechanics/setowner
  [SetParent]: /skills/mechanics/SetParent
  [SetProjectileDirection]: /skills/mechanics/SetProjectileDirection
  [SetProjectileBulletModel]: /skills/mechanics/setprojectilebulletmodel
  [SetRaiderPatrolBlock]: /skills/mechanics/setraiderpatrolblock
  [SetRaiderPatrolLeader]: /skills/mechanics/setraiderpatrolleader
  [SetRotation]: /skills/mechanics/setrotation
  [SetTarget]: /skills/mechanics/settarget
  [SetTargetScore]: /skills/mechanics/settargetscore
  [SetTongueTarget]: /skills/mechanics/settonguetarget
  [SetScore]: /skills/mechanics/setscore
  [SetSpeed]: /skills/mechanics/setspeed
  [SetStance]: /skills/mechanics/setstance
  [Shield]: /skills/mechanics/shield
  [ShieldPercent]: /skills/mechanics/shieldpercent
  [ShootFireball]: /skills/mechanics/shootfireball
  [ShootPotion]: /skills/mechanics/shootpotion
  [ShootSkull]: /skills/mechanics/shootskull
  [ShootShulkerBullet]: /skills/mechanics/shootshulkerbullet
  [ShowEntity]: /skills/mechanics/showentity
  [Signal]: /skills/mechanics/signal
  [Speak]: /skills/mechanics/speak
  [Spring]: /skills/mechanics/spring
  [StopUsingItem]: /skills/mechanics/stopusingitem
  [Stun]: /skills/mechanics/stun
  [Suicide]: /skills/mechanics/suicide
  [Summon]: /skills/mechanics/summon
  [SummonPassenger]: /skills/mechanics/summonpassenger
  [AddTag]: /skills/mechanics/addtag
  [RemoveTag]: /skills/mechanics/removetag
  [TakeItem]: /skills/mechanics/takeitem
  [Teleport]: /skills/mechanics/teleport
  [TeleportY]: /skills/mechanics/teleporty
  [TeleportIn]: /skills/mechanics/teleportin
  [TeleportTo]: /skills/mechanics/teleportto
  [Threat]: /skills/mechanics/threat
  [Throw]: /skills/mechanics/throw
  [ToggleLever]: /skills/mechanics/togglelever
  [ToggleSitting]: /skills/mechanics/togglesitting
  [UndoPaste]: /skills/mechanics/undopaste
  [Velocity]: /skills/mechanics/velocity
  [Weather]: /skills/mechanics/weather
  [WolfSit]: /skills/mechanics/wolfsit
  [在這裡查看所有可用特效]: /skills/effects/
  
  
  <!-- METAMECHANICS -->
  [Skill]: /skills/mechanics/skill
  [VariableSkill]: /skills/mechanics/variableskill
  [Aura]: /skills/mechanics/aura
  [CancelEvent]: /skills/mechanics/cancelevent
  [Cast]: /skills/mechanics/cast
  [Chain]: /skills/mechanics/chain
  [ChainMissile]: /skills/mechanics/chainmissile
  [Delay]: /skills/mechanics/delay
  [EndProjectile]: /skills/mechanics/endprojectile
  [GlobalCooldown]: /skills/mechanics/globalcooldown
  [Missile]: /skills/mechanics/missile
  [ModifyProjectile]: /skills/mechanics/modifyprojectile
  [OnAttack]: /skills/mechanics/onattack
  [OnDamaged]: /skills/mechanics/ondamaged
  [OnJump]: /skills/mechanics/onjump
  [OnShoot]: /skills/mechanics/onshoot
  [OnSwing]: /skills/mechanics/onswing
  [OnUse]: /skills/mechanics/onuse
  [Orbital]: /skills/mechanics/orbital
  [Polygon]: /skills/mechanics/polygon
  [Projectile]: /skills/mechanics/projectile
  [ProjectileVelocity]: /skills/mechanics/projectilevelocity
  [PlayBlockBreakSound]: skills/mechanics/PlayBlockBreakSound
  [PlayBlockFallSound]: skills/mechanics/PlayBlockFallSound
  [PlayBlockHitSound]: skills/mechanics/PlayBlockHitSound
  [PlayBlockPlaceSound]: skills/mechanics/PlayBlockPlaceSound
  [PlayBlockStepSound]: skills/mechanics/PlayBlockStepSound
  [Shoot]: /skills/mechanics/shoot
  [Slash]: /skills/mechanics/slash
  [Volley]: /skills/mechanics/volley
  [SudoSkill]: /skills/mechanics/sudoskill
  [RandomSkill]: /skills/mechanics/randomskill
  [SetSkillCooldown]: /skills/mechanics/setskillcooldown
  [Totem]: /skills/mechanics/totem
  [VariableAdd]: /skills/mechanics/variableadd
  [VariableMath]: /skills/mechanics/variablemath
  [SetVariable]: /skills/mechanics/setvariable
  [SetVariableLocation]: /skills/mechanics/setvariablelocation
  [VariableUnset]: /skills/mechanics/variableunset
  [VariableSubtract]: /skills/mechanics/variablesubtract
  [Swap]: /skills/mechanics/swap
  [Time]: /skills/mechanics/time
  [Hide]: /skills/mechanics/hide
  [TrackLocation]: /skills/mechanics/tracklocation
  [GiveItemFromSlot]: /skills/mechanics/giveitemfromslot
  [OnBlockBreak]: /skills/mechanics/onblockbreak
  [OnBlockPlace]: /skills/mechanics/onblockplace
  [OnSwing]: /skills/mechanics/onswing
  [OnInteract]: /skills/mechanics/oninteract
  [OnJump]: /skills/mechanics/onjump
  [OnDeath]: /skills/mechanics/ondeath
  [ShieldBreak]: /skills/mechanics/shieldbreak
  [Switch-Case]: /skills/mechanics/switch-case
  [SetFaction]: /skills/mechanics/setFaction