## 用途
將指定變量(Variable)中存儲的位置設為目標 [設定變量位置](/skills/mechanics/setvariablelocation)

## 細項設定

| 設定項      | 簡寫  | 用途            | 預設值 |
|----------------|----------|------------------------------------------------------------|:-------:|
| variable       | name, n, var, key, k | 變量名稱                      |         |
| scope          | s        | 變量類型|         |

## 範例
```yaml
ExampleSkill:
  Skills:
  - setvarloc{var=caster.1;v=@targetlocation} @self
  - e:p{y=2} @VariableLocation{var=caster.1}
```

## 簡化寫法
- [x] varLocation