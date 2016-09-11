名前 : Protospace

概要 : プロトタイプを見せれるユーザー投稿型サービス

テーブル設計

1,productsテーブル

アソシエーション
--------------
belongs_to :uses
has_many :comment
has_many :image
--------------

カラム
--------------
title : string
copy : string
concept : text
created_at : timestamp
update_at : timestamp
user_id : integer
image_id : integer
---------------

2,userテーブル
---------------
has_many :products
has_many :comments
---------------

カラム
---------------
name : string
e-mail : device自動
passward : device自動
user_image_url : text
member : string
profyle : text
works : text
created_at : timestamp
update_at : timestamp
----------------

3,commentテーブル

アソシエーション
----------------
belongs_to :product
belongs_to :user
----------------

カラム
----------------
comment : text
product_id : integer
user_id : integer
created_at : timestamp
update_at : timestamp
----------------

4,imageテーブル

アソシエーション
----------------
belongs_to :product
----------------

カラム
----------------
proto_image_url :text
product_id : integer
----------------
