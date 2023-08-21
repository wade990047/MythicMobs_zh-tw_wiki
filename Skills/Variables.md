變量
=======

變量是儲存資料的系統之一。

使用變量，你可以儲存和操作之後要在佔位符或條件中使用的值。這些值可以是永久或臨時的。

### 變量類型

變量可以是多種類型之一，類型是在使用 **[設置變量](/skills/mechanics/setvariable)** 技能時所定義的。 

類型通常是可以互相轉換的，MythicMobs 會將變量應用於所要求的任何情況，但有可能會輸出警告，如果嘗試將變量用於沒有意義的事情，則會出現錯誤。

**可用的類型**:

| **類型** | **用途**  |
|----------|----------------------------------|
| INTEGER  | 整數 |
| FLOAT| 浮點數(小數)|
| STRING   | 字串  |

### 變量儲存位置

變量的 **`scope`** 是該變量存在的 **`位置`**

並非所有範圍都適用於所有情況(例如，條件可能沒有施法者，但施法者是條件的目標)

**變量可用位置(scope)**:

| **位置** | **實際存在目的地**|
|----------|------------------------------------------|
| SKILL    | 存在技能樹下，技能結束時變量跟著消失 |
| CASTER   | 存在施法者上 |
| TARGET   | 存在於目標上 |
| WORLD    | 存在當前世界 |
| GLOBAL   | 存在全伺服器 |


### 應用

所有變量技能和條件都接受 **var=** 和 **scope=** 設定來確認要使用的變量以及在何處使用。

可以使用 **`var=scope.variable_name`** 縮寫位置。

下方範例代表相同的內容：

```yml
設置變量:
  Skills:
  - setvariable{var=target.somevariable; ...}
  - setvariable{var=somevariable;scope=target; ...}
```

### 變量相關技能

變量技能是利用變量的特殊技能。

技能可以指定實體、位置或空，不同目標會影響技能執行結果，具體取決於你所使用的位置。

例如，如果不以實體為目標，則嘗試獲取目標的變量當然會失敗。

| 技能 | 用途 |
|--------------|-----------------|
| [SetVariable](/skills/mechanics/setvariable)   | 創建並設置初始變量 |
| [SetVariableLocation](/skills/mechanics/setvariablelocation)   | 在目標位置設置變量 |
| [VariableUnset](/skills/mechanics/variableunset)   | 刪除並取消指定變量 |
| [VariableAdd](/skills/mechanics/variableadd)   | 增加指定的變量數值  |
| [VariableSubtract](/skills/mechanics/variablesubtract) | 減少指定的變量數值   |
| [VariableMath](/skills/mechanics/variablemath) | 數字變量做數學運算 |

### 變量相關條件

| 條件 | 用途 |
|-----------------|------------------|
| [Variable Equals](/skills/conditions/variableequals)| 變量是否等於指定值 |
| [Variable Is Set](/skills/conditions/variableisset) | 變量是否有成功設置   |
| [Variable In Range](/skills/conditions/variableinrange) | 變量數值是否在範圍內 |

### 變量的佔位符

變量可以在任何允許佔位符的 MythicMobs 技能或值中使用。

通常使用格式 **`scope.var.variable`** 來完成

使用佔位符變量時，也可以使用語法 **`scope.var.variable|default`** 

指定在變量未定義時使用的 **`"default"(默認)`** 值

### 範例 

在下面的範例中，NPC 如果被沒有設置"title"變量的人右鍵單擊互動。

將對觸發者發送訊息："你好啊，流浪者"，

```yml
- message{m="你好啊, <target.var.title|流浪者>"} @trigger ~onInteract
```
但是，如果為目標加上 "title" 變量並設置為 "勇者"：
```yml
- setVariable{var=target.title;value="勇者"} @trigger ~onInteract
```
則在未來都沒有變更 "title" 變量的情況下，NPC 被互動後所送出的訊息就會是："你好啊，勇者"