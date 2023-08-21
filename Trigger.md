Triggers (觸發器) 是用來決定一項技能他應該要在什麼樣的條件下被觸發.

<u>**觸發器不能在支線技能中使用**</u>
若要使用觸發器，必須要在生物或物品底下的Skills中直接使用.

**可用的觸發器列表:**

| 觸發器                                | 觸發條件                                            |
|----------------------------------------|--------------------------------------------------------------|
| onCombat                               | 預設                                             |
| [onAttack](#onattack)                  | 當怪物攻擊到其他生物時                                 |
| [onDamaged](#ondamaged)                | 當怪物受傷時                                      |
| [onSpawn](#onspawn)                    | 當怪物重生/召喚時                                          |
| [onDespawn](#ondespawn)                | 當怪物消失時(區塊清除、自然消失)                                    |
| [onReady / onFirstSpawn](#onready)                    | 當怪物第一次從刷怪籠中生成     |
| [onLoad](#onload)                      | 當怪物被讀取時 (重新啟動伺服器後的生成或加載) |
| [onDeath](#ondeath)                    | 當怪物死亡時                                           |
| [onTimer:*#*](#ontimerticks)           | 每 \# ticks 執行一次 (\# 輸入ticks 每 20ticks 為一秒)           |
| [onInteract](#oninteract)              | 當怪物被右鍵互動時                                |
| [onPlayerKill](#onplayerkill)          | 當怪物擊殺玩家時                                  |
| [onEnterCombat](#onentercombat)        | 當怪物進入戰鬥狀態時 (需要啟用 threat tables(威脅表))    |
| [onDropCombat](#ondropcombat)          | 當怪物離開戰鬥狀態時 (需要啟用 threat tables(威脅表))    |
| [onChangeTarget](#onchangetarget)      | 當怪物變更攻擊目標時 (需要啟用 threat tables(威脅表))  |
| [onExplode](#onexplode)                | 當怪物爆炸時 (只適用於苦力怕/TNT)     |
| [onPrime](#onprime)                    | 當怪物預備爆炸時 (只適用於苦力怕/TNT)                 |
| [onCreeperCharge](#oncreepercharge)    | 當苦力怕被充能時 (閃電打中苦力怕)  |
| [onTeleport](#onteleport)              | 當怪物傳送時    |
| [onSignal:*[signal]*](#onsignalsignal) | 當怪物接收到信號時                               |
| [onShoot](#onshoot)                    | 當怪物射出導彈類攻擊時(箭矢、燃燒彈)                              |
| [onTame](#ontame)                      | 當怪物被馴服時                                      |
| [onBreed](#onbreed)                    | 當怪物繁殖時                        |
| [onTrade](#ontrade)                    | 當村民完成一筆交易時(伺服器端必須要是 Paper)          |
| [onChangeWorld](#onchangeworld)        | 當怪物切換世界時                                   |
| [onBucket](#onbucket)                  | 當牛被擠牛奶時 / 水中生物被裝進鐵桶時 (蠑螈、河豚等等...)             |

<!--
ADD THIS TRIGGER BACK WHEN IT WORKS

| onKill                       | When something kills a mob                                   |
-->

如何使用觸發器
--------------

觸發器在生物/物品配置的技能部分中使用，
並且必須在前面加上波浪號 (~)。
另外若是使用onTimer，必須要加入ticks的設定。
```yml
SkeletalWizard_Fire:
  Type: WITHER_SKELETON
  Display: '&Skeletal Fire Wizard'
  Health: 50
  Damage: 0.5
  Skills:
  - ignite{ticks=100} @target ~onAttack
  - skill{s=FireShield} @trigger ~onDamaged 0.1
  - skill{s=AOEFire} ~onTimer:300
```

以下是在上面這個範例中，每項技能的詳細解釋

當怪物攻擊到目標時，將會觸發點燃(ignite)的技能效果，並且持續五秒

當怪物被攻擊時將會對技能的觸發者使用FireShiled的技能，技能觸發的機率是 10%

怪物每 15秒 會使用一次AOEFire的技能

不使用觸發器會怎麼樣?
---------------------

觸發器可以更加靈活地確定何時技能應該施放 

**強烈** 建議所有的技能都使用觸發器

而不是使用預設的觸發器來施放技能

當你的技能沒有設定觸發器時, 預設的觸發器會使用 `~onCombat`
他會在以下的條件下觸發你的技能:
- 當怪物造成傷害或是受到傷害時
- 當怪物生成時
- 當怪物死亡時

<!-- -->
```yml
SkeletalWarrior:
  Mobtype: skeleton
  Display: '<blue>A Skeletal Warrior</blue>'
  Skills:
  - skill{s=Bash} =10%-90%
```
在上面這個範例中，
只要怪物在血量 10% ~ 90% 之間受到傷害或是造成傷害，都會觸發技能

關於目標選擇器 @trigger 
---------------------

你應該有注意到在剛剛的範例中有使用到 `@trigger` 這個目標選擇器
並且也有列在 [目標選擇器](/Skills/Targeters) 這個頁面當中
`@trigger` 他所指定的目標是：**導致**這個技能被啟用的目標
例如當玩家攻擊一隻怪物，觸發了~onDamaged的技能，那這時候`@trigger`的目標就是指定在玩家身上
假設今天有一隻怪物發送了信號給目標怪物，那`@trigger`的目標就會是發送信號的怪物
以此類推

所有可用的觸發器
----------------------
#### ~onSpawn
當怪物生成時觸發，無法套用 `@trigger`.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當怪物生成時，對當前世界的所有玩家發送訊息
    - message{m=SPAWN} @World ~onSpawn
```

#### ~onDeath
當怪物死亡時觸發. `@trigger` 的目標是擊殺怪物的人/生物 <br>

如果伺服器端是Paper，只需要配合**cancelevent**機制就可以取消死亡事件(範例2)。

此後生物的生命值將基於`ReviveHealth`選項中指定的內容。
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當怪物死亡時，對當前世界的所有玩家發送訊息
    - message{m=DEATH} @World ~onDeath
```
```yaml
ImmortalCow:
  Type: COW
  Display: '&eImmortal Cow'
  Health: 20
  Options:
    ReviveHealth: -1
  Skills:
  - skill{s=[
    - cancelevent
    - e:p{p=HEART;hs=0.5;vs=0.5;y=1.5}
    - speak{m=Call an ambulance, but not for me!}
    ];sync=true} @self ~onDeath
```
#### ~onAttack
當怪物攻擊到目標時觸發.

`@trigger` 的目標是因攻擊而受到傷害的生物.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Damage: 1
  Skills:
    # 當怪物攻擊到目標時，對當前世界的所有玩家發送訊息
    - message{m=ATTACK} @World ~onAttack
```

#### ~onDamaged
受到攻擊時觸發.

`@trigger` 的目標是造成傷害的實體.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當怪物受到傷害時，對當前世界的所有玩家發送訊息
    - message{m=DAMAGED} @World ~onDamaged
```

#### ~onDespawn
當怪物消失時觸發.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當怪物消失時，對當前世界的所有玩家發送訊息
    - message{m=DESPAWNED} @World ~onDespawn
```

#### ~onExplode
實體爆炸時觸發.

mobGriefing(防爆) 必須要關閉才可以確保這項觸發器能夠正常運作.
```yml
EXAMPLE_MOB:
  Type: CREEPER
  Skills:
    # 當怪物爆炸時，對當前世界的所有玩家發送訊息
    - message{m=EXPLODE} @World ~onExplode
```

#### ~onTeleport
傳送時觸發.
```yml
EXAMPLE_MOB:
  Type: ENDERMAN
  Skills:
    # 當怪物傳送時，對當前世界的所有玩家發送訊息
    - message{m=TELEPORT} @World ~onTeleport
```

#### ~onTimer:[tick(s)]
每 *n* ticks 執行一次技能. Ticks 不能為 0 並且每 20ticks 為一秒

**使用此觸發器時務必小心，因為它可能導致伺服器/用戶端效能問題。**

**例如超大量的粒子效果可能會導致用戶端嚴重延遲(爆ping)，有機率將用戶直接從伺服器中踢出**
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 每 0.05 秒，對當前世界的所有玩家發送訊息
    - message{m=TIMER every tick (0.05 seconds)} @World ~onTimer:1
    # 每 2 秒，對當前世界的所有玩家發送訊息
    - message{m=TIMER every 40 ticks (2 seconds)} @World ~onTimer:40
```

#### ~onPlayerKill
擊殺玩家時觸發.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 擊殺玩家後，對當前世界的所有玩家發送訊息
    - message{m=PLAYER KILLED} @World ~onPlayerKill
```

#### ~onEnterCombat
當怪物進入戰鬥狀態時觸發. **[威脅表](/Mobs/ThreatTables) 必須是啟用狀態**
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Modules:
    ThreatTable: true
  Skills:
    # 進入戰鬥狀態後，對當前世界的所有玩家發送訊息
    - message{m=ENTERED COMBAT} @World ~onEnterCombat
```

#### ~onDropCombat
當怪物離開戰鬥狀態時觸發. **[威脅表](/Mobs/ThreatTables) 必須是啟用狀態**
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Modules:
    ThreatTable: true
  Skills:
    # 離開戰鬥狀態後，對當前世界的所有玩家發送訊息
    - message{m=DROPPED COMBAT} @World ~onDropCombat
```

#### ~onChangeTarget
當怪物切換目標時觸發. **[威脅表](/Mobs/ThreatTables) 必須是啟用狀態**
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Modules:
    ThreatTable: true
  Skills:
    # 當怪物切換目標時，對當前世界的所有玩家發送訊息
    - message{m=Target Changed} @World ~onChangeTarget
```

#### ~onInteract
當怪物和玩家有互動或是 *右鍵點擊* 怪物時觸發.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當怪物和玩家有互動，對當前世界的所有玩家發送訊息
    - message{m=INTERACTED} @World ~onInteract
```

#### ~onSignal:[signal]
當怪物接收到信號時觸發.

[信號](/Skills/mechanics/signal) 技能

信號必須由字母/數字/基本符號組成.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當與玩家與怪物互動後，對半徑64格內的所有生物發送信號(MOO_FOR_ME)
    - signal{s=MOO_FOR_ME} @EIR{r=64} ~onInteract
```

```yml
DUMMY_MOB:
  Type: COW
  Skills:
    # 當怪物接收到信號(MOO_FOR_ME)時，對當前世界的所有玩家發送訊息
    - message{m=MOO} @World ~onSignal:MOO_FOR_ME
```

當然你也可以不要特別指定要接收到哪個信號

下面的範例是當每次接收到任意信號時都會觸發
```yml
DUMMY_MOB:
  Type: COW
  Skills:
    # 當怪物接收到信號時，對當前世界的所有玩家發送訊息
    - message{m=MOO...?} @World ~onSignal
```


#### ~onShoot
射出子彈時觸發.

例如：骷髏弓箭手用弓射出箭矢時; EOE, 烈焰使者, 終界龍射出火球時.
```yml
EXAMPLE_MOB:
  Type: SKELETON
  Skills:
    # 當怪物射出子彈時，對當前世界的所有玩家發送訊息
    - message{m=I SHOT AN ARROW} @World ~onShoot
```

#### ~onBreed
當生物繁殖時觸發.

這個觸發器擁有 `@Father` 與 `@Mother` 的目標選擇器.
```yml
EXAMPLE_MOB:
  Type: CHICKEN
  Skills:
    # 當生物繁殖時，對當前世界的所有玩家發送訊息
    - message{m=LET'S GET THIS BREAD} @World ~onBreed
```

#### ~onTame
當玩家馴服生物時觸發.
```yml
EXAMPLE_MOB:
  Type: WOLF
  Skills:
    # 當玩家馴服生物時，對當前世界的所有玩家發送訊息
    - message{m=I GOT TAMED} @World ~onTame
```

#### ~onCreeperCharge
當苦力怕被充能時觸發.
```yml
EXAMPLE_MOB:
  Type: CREEPER
  Skills:
    # 當苦力怕被充能時，對當前世界的所有玩家發送訊息
    - message{m=CHARGED} @World ~onCreeperCharge
```

#### ~onPrime
當實體預備爆炸時觸發
```yml
EXAMPLE_MOB:
  Type: CREEPER
  Skills:
    # 當實體預備爆炸時，對當前世界的所有玩家發送訊息
    - message{m=OOO I'M GONNA EXPLODE} @World ~onPrime
```

#### ~onTrade
當村民與玩家交易時觸發.
```yml
EXAMPLE_MOB:
  Type: VILLAGER
  Skills:
    # 當村民與玩家交易時，對當前世界的所有玩家發送訊息
    - message{m=TRADED} @World ~onTrade
```

#### ~onReady
當生物準備從刷怪籠生成時觸發. [刷怪籠](Spawners)
```yml
EXAMPLE_MOB:
  Type: VILLAGER
  Skills:
    # 當生物準備從刷怪籠生成時，對當前世界的所有玩家發送訊息
    - message{m=READY TO SPAWN FROM A SPAWNER} @World ~onReady
    - message{m=READY TO SPAWN FROM A SPAWNER} @World ~onFirstSpawn
```

#### ~onLoad
當生物在伺服器重啟後被讀取時觸發.
```yml
EXAMPLE_MOB:
  Type: VILLAGER
  Skills:
    # 當生物在伺服器重啟後被讀取時，對當前世界的所有玩家發送訊息
    - message{m=LOADED} @World ~onLoad
```

#### ~onChangeWorld
當怪物切換世界時觸發.
```yaml
WorldJumper:
  Type: WITHER_SKELETON
  Skills:
  # 當怪物切換到世界world_the_end時，讓自己使用指令/say The End!
  - command{c=say The End!} @self ~onChangeWorld ?varEquals{var=skill.world;value=world_the_end}
  # 當怪物切換到世界world_nether時，讓自己使用指令/say The Nether!
  - command{c=say The Nether!} @self ~onChangeWorld ?varEquals{var=skill.world;value=world_nether}
```

#### ~onBucket 
當牛被擠奶或是生物被裝進鐵桶時觸發.
```yaml
ANormalCow:
  Type: Cow
  Skills:
  - skill{s=[
    - message{m="HOW DARE YOU?!?"} @trigger
    - sound{s=entity.creeper.primed}
    - explosion{yield=5;delay=30}
    ];cd=2} @self ~onMilk
```