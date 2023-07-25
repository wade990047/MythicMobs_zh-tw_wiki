## 用途
Tests the difficulty scale at the target location.
 

## 細項設定
| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----------------------------------------------------------------------|---------|
| difficulty| diff, d   | The difficulty range to check   | |

 
## 範例
```yaml
  Conditions:
  - localdifficulty{d=>0}
```