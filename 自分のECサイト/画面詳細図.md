### 画面詳細図
## トップページ
### プロトタイプは以下のリンク先
[プロトタイプ](https://www.figma.com/file/W9QCNXyBwxticc2lhgeHdI/%E8%87%AA%E5%88%86%E3%81%AEEC%E3%82%B5%E3%82%A4%E3%83%88?node-id=6%3A2)
*****
<img src="../img/toppage.png" width="500">

*****
補足:対応DBの列はDB設計後、〇を対応するテーブル・カラム名に差し替えること。

|id|要素|内容|アクション|イベント|対応DB|
|---|---|---|--|--|---|
|1|ロゴ|テキスト|-|-|-|
|2|検索バー|テキストボックス|テキスト入力|-|item-itemname|
|3|検索ボタン|ボタン|クリック|検索実行|item-itemname,itemmany|
|4|ログイン|ボタン|クリック|ログインページに遷移|-|
|5|カート|ボタン|クリック|カートページに遷移|item-itemname,itemmany,itemquanty|
|6|サインアウト|ボタン|クリック|サインアウトする|userid|
|7|商品名|テキスト|クリック|商品詳細|itemname|
|8|金額|テキスト|-|-|-|
|9|次へ|ボタン|クリック|次のページへ|item-itemname,itemmany|
