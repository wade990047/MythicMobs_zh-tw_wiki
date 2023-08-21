## 用途
[變量](/Skills/Variables) 是否有成功設置

## 細項設定

| 技能名稱 | 簡化寫法| 用途 | 預設值 |
|-----------|-----------|----|---------|
| variable  | n, var  | 要檢查的變量名稱   | |

## 範例

```yml
  Conditions:
  - variableisset{var=target.dazed} true
```