## 用途

對目標造成傷害

## 細項設定
| 設定項 | 簡化寫法 | 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| amount| a | 造成傷害量| 1   |
| ignoreArmor | ia, i   | 是否無視盔甲防禦，但仍然會計算由附魔產生的保護| false   |
| preventknockback | pkb, pk | 是否防止擊退| false   |
| preventimmunity  | pi  | 是否無視傷害冷卻| false   |
| element   | e, damagetype, type | 設置傷害屬性| |
| damagecause | dc, cause | 設置這項傷害的傷害來源.<br/> (僅適用於版本 1.17+)   | entity_attack |
| ignoreenchantments |ignoreenchants, ie  | 是否忽略附魔.<br>(僅適用於版本 1.19+) | false |
| noanger   | na|是否讓被傷害的生物生氣| false   |
| ignoreinvulnerability | ignoreinvulnerable, ii | 是否忽略無敵| false   |
| ignoreshield | is | 是否忽略舉盾   | false   |
| damageshelmet| dh | 是否影響頭盔耐久度  | false   |
| ignoreeffects| ieff   | 是否無視藥水效果| false   |
| ignoreresistance | ir | 是否忽略抗性  | false   |

### 傷害來源 (DamageCause)
這項設定只適用於 MM v5.0 以後的版本，
可使用的來源類型都在 [Spigot文件](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/entity/EntityDamageEvent.DamageCause.html) 中

筆記: 只有 `entity_attack`, `entity_sweep_attack`, `thorns`, `sonic_boom`, `entity_explosion`, 和 `projectile` 會回傳實體傷害, 
這代表 `<trigger.name>` 會回傳 "Unknown"

### 傷害屬性 (Elements)
向上面提到的, 可以為 傷害(Damage) 技能設置一個 "element" 如下:

```yml
- damage{amount=10;element=FIRE} @target ~onUse
- damage{amount=10;element=ICE} @target ~onUse
```

"element"可以命名為任何東西，也可以被使用在怪物的**傷害倍率器(DamageModifiers)**中，來決定對於這種傷害的該獲得多少的攻擊倍率
```yml
DamageModTest: 
  Type: COW 
  DamageModifiers:
  - LIGHTNING 0.1
  - FIRE 2.0
  - AIR 1.0
  - ICE 0.5 
  Skills:
  - message{m="Damaged by <skill.var.damage-type> for <skill.var.damage-amount>"} @PIR{r=50} ~onDamaged
```
這項設定也可以用在 "onDamaged" 光環, 設定方式是 `damageMods="FIRE 0.5"`

## 範例
```yml
  Skills:
  - damage{amount=20;ignoreArmor=true} @target ~onTimer:20
```
將在每秒對目標造成20點無視盔甲保護的傷害

```yml
FreezeBlast:
  Skills:
  - effect:sound{s=block.fire.extinguish;v=1;p=0.5} @PIR{r=6}
  - effect:particles{p=explode;a=8;vs=0.5;hs=0.5;s=0;y=1;repeat=5;repeatInterval=20} @PIR{r=6}
  - effect:particles{p=drip_water;a=10;vs=0.5;hs=0.5;s=0;y=1;repeat=5;repeatInterval=20} @PIR{r=6}
  - potion{t=SLOW;d=120;l=6} @PIR{r=6}
  - damage{a=120;pkb=true} @PIR{r=6}
```
對**傷害(Damage)**技能更複雜的使用可以給人一種高級的感覺

就像上面的例子。它使用特效來製作生物的目標看起來就像是被粒子凍結了

(在重複間隔也可以產生一種揮之不去的冰凍效果) 

並造成 7 級緩速(-105% 移動速度)
另外對半徑6格內的玩家造成 120 點傷害

##

**付費版範例**
```yml
  Skills:
  - damage{amount=<caster.var.somevariable> * 0.5 + 1} @target ~onTimer:20
```
這項技能用了變量即造成 "<caster.var.somevariable> * 0.5 + 1" 傷害
假設: <caster.var.somevariable> 的值是 5,

那就會造成```5*0.5+1 => 2.5+1 => 3.5點傷害```


## 簡化寫法
- [x] d