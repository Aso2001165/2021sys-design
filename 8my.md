```uml
@startuml
ユーザー -> wedサーバー : 登録情報
webサーバー　-> DB : 登録情報検索
DB -> DB : 検索処理
DB -> webサーバー : 結果出力
alt ID,アドレスの値の重複なし
webサーバー -> ユーザー : アカウント作成
else
webサーバー -> ユーザー : エラーを出力
end
@enduml
```
