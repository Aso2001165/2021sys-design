# DB定義書
## ER図
[ER図]( https://github.com/Aso2001165/2021sys-design/blob/main/ER_all.md "ER図はこちら" )


## DBテーブルカラム詳細一覧


# データベース詳細


### d_qurchase(購入テーブル)
|属性名|型|PK|NN|FK|
|---|---|---|---|---|
|order_id|bigint(20)|〇|〇|-|
|customer_code|varchar(50)|-|〇|-|
|purchase_date|date|-|〇|-|
|total_price|int(11)|-|〇|

### d_qurchase_detail(購入テーブル詳細)
|属性名|型|PK|NN|FK|
|---|---|---|---|---|
|detail_id|bigint(20)|〇|〇|-|
|order_id|bigint(20)|-|〇|〇|
|item_code|imt(11)|-|〇|-|
|price|int(11)|-|〇|-|
|price|int(11)|-|〇|-|

### m_customers(ユーザー(顧客)テーブル)
|属性名|型|PK|NN|FK|
|---|---|---|---|---|
|customers_code|varchar(50)|〇|〇|-|
|pass|varchar(50)|-|〇|-|
|name|varchar(20)|-|〇|-|
|addres|varchar(100)|-|〇|-|
|tel|varchar(20)|-|〇|-|
|mail|varchar(100)|-|〇|-|
|del_flag|int(1)|-|〇|-|
|reg_date|date|-|〇|-|

### m_category(カテゴリテーブル)
|属性名|型|PK|NN|FK|
|---|---|---|---|---|
|category_id|int(11)|〇|〇|-|
|name|varchar(20)|-|〇|-|
|reg_date|date|-|〇|-|

### m_items(商品テーブル)
|属性名|型|PK|NN|FK|
|---|---|---|---|---|
|item_code|int(11)|〇|〇|-|
|item_name|varchar(50)|-|〇|-|
|price|int(11)|-|〇|-|
|category_id|int(11)|-|〇|〇|
|image|varchar(200)|-|〇|-|
|detail|varchar(500)|-|-|-|
|del_flag|int(11)|-|-|-|
|reg_date|date|-|〇|-|
