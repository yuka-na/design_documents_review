# テーブル定義書1
## 全体
- 主キーは~idという命名規則ではなくid
- テーブル名が全部大文字、スネークケースで書かれていない
- カラム命名規則(adminテーブルのadmin_emailカラムではなくadminテーブルのemaiカラム)
- 複数単語のカラムがスネークケースで書かれていない(スペースまたは１単語扱いで書かれている)

## user
- l_name,f_name等意味合いを省略して書くとカラムの役割がわかりづらい
- 郵便番号電話番号はintegerではなく、string型
- メンバーステータスの命名規則、ユーザー情報なのに急にメンバーになるのはおかしい
- メンバーステータスのデータ種類は限られているのでintegerでenumとかで管理すべき
- ship_addressでは他住所を1ユーザーにつき1つしか登録できない

## products
- disc_idがある(ディスクが親テーブルとなっている)
- genre_id,label_id,artist_idにFKがない
- CD画像カラム、refileを使用するなら後ろにidをつけて型をintegerにする(carrierwaveならこれで可能)
- notax_priceカラムはno_tax_priceにすると良い、というかここは単純にpriceでいいと思う

## discs
- productのidがあること自体はあっているがそうなるとproductにdisc_idがあるのでおかしくなる
- products_idではなくproduct_id
- track_numの命名がわかりづらい

## songs
- 曲順を識別するカラムがない

## labels
- products_idではなくproduct_id
labelカラムをnameに

## artists
- products_idではなくproduct_id
artistカラムをnameに

## genres
- products_idではなくproduct_id
gerneカラムをnameに

## cart_items
- products_idではなくproduct_id、データ型無し
- 小計はCD情報から引っ張れるのでいらない
- buy numの命名がわかりづらい

## buy_details
- 管理者目線なのでテーブル名が不適切
- buy numの命名がわかりづらい
- CDと紐づいてない

## buy
- 管理者目線なのでテーブル名が不適切
- buy_detailと関係性が逆
- payの命名がわかりづらい、データ型はenumを使って切り替えるのならinteger
- stockの命名がわかりづらい
- buy_atの命名がわかりづらい
- 郵便番号を格納するカラムがない