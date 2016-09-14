名前 : Protospace

概要 : プロトタイプを見せれるユーザー投稿型サービス

テーブル設計

1,productsテーブル  
アソシエーション
~~~~~~~~~~~~~~~  
belongs_to :user  
has_many :comments  
has_many :images  
has_many :likes
~~~~~~~~~~~~~~~  
カラム  
~~~~~~~~~~~~~~~  
title : string  
copy : string  
concept : text  
created_at : timestamp  
update_at : timestamp  
user_id : references  
image_id : references  
~~~~~~~~~~~~~~~  
2,usersテーブル  
アソシエーション  
~~~~~~~~~~~~~~~  
has_many :products  
has_many :comments  
belongs_to :like
~~~~~~~~~~~~~~~  
カラム  
~~~~~~~~~~~~~~~  
name : string  
e-mail : device自動  
passward : device自動  
user_image_url : text  
member : string  
profyle : text  
works : text  
created_at : timestamp  
update_at : timestamp  
~~~~~~~~~~~~~~~  
3,commentsテーブル  
アソシエーション  
~~~~~~~~~~~~~~~  
belongs_to :product  
belongs_to :user  
~~~~~~~~~~~~~~~  
カラム  
~~~~~~~~~~~~~~~  
comment : text  
product_id : references  
user_id : references  
created_at : timestamp  
update_at : timestamp  
~~~~~~~~~~~~~~~  
4,imagesテーブル  
アソシエーション  
~~~~~~~~~~~~~~~  
belongs_to :product  
~~~~~~~~~~~~~~~  
カラム  
~~~~~~~~~~~~~~~  
url :text  
product_id : references  
~~~~~~~~~~~~~~~  
5,likesテーブル  
アソシエーション  
~~~~~~~~~~~~~~  
belongs_to :product  
has_many :users  
~~~~~~~~~~~~~~  
カラム  
~~~~~~~~~~~~~~  
product_id : references
user_id : references
