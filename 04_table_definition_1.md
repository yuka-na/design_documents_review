# テーブル定義書1
## 全体
- 自分以外の住所(配送先住所)を格納する場所がない
- PKは table_id とするべきか、単に id とするべきか (わかりやすいようにあえてそう書いているのか？)(ex: book.book_id ではなく book.idとアクセスするため)
- ↑ この通りであれば全てのテーブル名を table_id → id

## Users
- user_f_name, user_f_kanaにNOT NULLがかかっていない
- 名前(性) → 名前(姓)
- DEFAULTがFALSEになっているのでデータ型は string → boolean(またはintegerにして、備考欄にenumで管理を追加)

## Buy
- 購入日カラムが不要
- テーブル名をBuy → Buys
- 配送ステータスがない
- 支払い方法カラムはenumで管理した方が楽(データ型をstring → integer)

## Buy details
- テーブル名をBuy details → Buy_details

## Cart item
- テーブル名をCart item → Cart_items
- カラム名をbuy num → buy_number
- PKがない

## Genre
- PKがない
- テーブル名をGenre → Genres
- genreカラムのカラム名をnameやgenre_nameに変更
- ジャンル名のデータ型を integer → string

## Aritists
- PKがない
- artistカラムのカラム名をnameやartist_nameに変更
- アーティスト名のデータ型を integer → string

## Labels
- PKがない
- labelカラムのカラム名をnameやlabel_nameに変更

## Admin
- テーブル名をAdmin → Admins
- PKがない

## Products
- カラム名をnotax_price → no_tax_price(税は購入時に追加するので単にpriceでも良い)
- disc_idカラムが不要
- genre_id, label_id, artist_idのFKに○を追加
- 在庫数カラムを削除して、入荷数カラムを追加
- 在庫ステータスカラムが不要
- ジャケット画像のNOT NULLが空なのはジャケット画像が入手しにくい状況が想定されるからなのか？(そのためのDEFAULT="画像準備中")

## Discs
- track_num → disc_num にカラム名を変更

## Songs
- PKがない
- songカラムのカラム名をnameやsong_nameに変更
- 曲名のデータ型を integer → string

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
