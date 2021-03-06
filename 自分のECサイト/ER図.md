```uml
@startuml
/'
  図の中で目立たせたいエンティティに着色するための
  色の名前（定数）を定義できます。
  ↓色のサンプル↓
  https://github.com/shibakay/2021sys-design/blob/main/color.md
'/

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

'グラデーションさせる場合 #xx-xx
!define MAIN_ENTITY #MintCream-MistyRose

/'
  デフォルト色を"skinparam class"で設定します。
'/
skinparam class {
    '図の背景
    BackgroundColor Snow
    '図の枠
    BorderColor Black
    'リレーションの色
    ArrowColor Black
}

package "ECサイト" as target_system {
    /'
      マスターテーブルを M、トランザクションを T などで表記
      １文字なら "主" とか "従" など日本語でも記載可能
     '/

    entity "顧客マスタ" as customer <m_customers> <<M,MASTER_MARK_COLOR>> {
        + customer_code [PK]
        --
        pass
        name
        address
        e-mail
        del_flag
        reg_date
    }

entity "カテゴリマスタ" as category <m_category> <<M,MASTER_MARK_COLOR>>{
+ category_id[PK]
--
name
reg_date

}

entity "商品マスタ" as items <m_items><<M,MASTER_MARK_COLOR>>{
+ item_code[PK]
--
item_name
price
# category_id[FK]
image
detail
del_flag
reg_date

}

entity "購入テーブル" as purchase<d_purchase><<T,TRANSACTION_MARK_COLOR>>{
+ order_id[PK]
--
customer_code
purchase_date
total_price
}

entity "購入テーブル詳細" as purchase_detail<d_purchase_detail><<T,TRANSACTION_MARK_COLOR>>{
+ detail_id[PK]
--
price
num
}

customer|o-o{purchase
purchase||-|{purchase_detail
purchase_detail}-do-||items
category||-o{items

  }
@enduml
```
