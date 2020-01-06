# テーブル定義書2
## 全体
- sellsとsell_detailsテーブルの親子関係が逆
- 全てのテーブルのPKを テーブル名_id → id (book.idのようにアクセスするため)

## users
- user_l_name → last_name(userを含める意味がない ← adminにはないため、lのみだとわかりずらい、user_f_name, user_l_kana, user_f_kanaも同様)
- member_status → status
- 退会ステータスカラムでデータ型がintegerなのでDEFAULT値はFALSEではなく0などにする

## products
- cd_title → title 
- notax_price → no_tax_price
- 在庫数カラムが不要で代わりに入荷数カラムが必要(入荷数から計算できるため)

## discs
- products_id → product_id

## songs
- 曲名カラムの名前がテーブル名と同じ song → titleなどに変更
- トラックナンバー → 曲順 track_num → number

## labels
- レーベル名カラムの命名を label → name (テーブル名とカラム名が被るから)

## artists
- アーティスト名カラムの命名を artist → name (テーブル名とカラム名が被るから)

## genres
- ジャンル名カラムの命名を genre → name (テーブル名とカラム名が被るから)

## cart items
- テーブル名をcart items → cart_items
- PKを Cart item_id → id
- カラム名をbuy num → buy_number
- products_id → product_id

## sell_details
- product_idにFKがついていない
- FKである sell_id がない(親テーブルとの結びつきがない)
- 値段を格納するカラムがない(変更してしまうときのことを考え、購入時の値段を格納するカラムが必要)
- products_id → product_id

## sells
- sell_details_idが不要(親子関係が逆)
- 支払い方法カラムで pay → pay_method
- 住所関連カラムの説明で送付先か配送先かで統一する

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
