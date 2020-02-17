# テーブル定義書1
## 全体
- 主キーになるカラムはidでよい。
- テーブル名はすべて小文字で良い。
- 命名規則、Genre -> genres, Cart item -> cart_items, Buy -> buys, Buy details -> buy_details
- Songs,Labels,Artists,Genre,Cart itemテーブルに主キーがない。
## Adminテーブル
- 管理者IDのPK漏れ
- 管理者IDのAUTOINCREMENTが抜けている。

## Usersテーブル
- user_l,user_fではなにを示しているかわからない。
- 名前（名、名カナ）にNOT NULL がついていない。
- 郵便番号はstring型であるべき。
- 電話番号も同様。
- user_~というuser_の接頭辞は必要ない。
- member_statusのデータ型がstringになっている。
-
## Productsテーブル
- disc_idがある。
- genre_id,label_id,artist_idのFK漏れ
- products_idというように複数形になってしまっている。


## Artists,Genre,Cart item,Songsテーブル(共通)
- FKにAUTOINCREMENTがついている。

## Artistsテーブル
- アーティスト名がinteger型になっている。

## Genreテーブル
- ジャンル名がinteger型になっている。

## Buy,Buy detailsテーブル(共通)
- buy num -> buy_num

## Buyテーブル
- buy_details_idは必要ない。
- 支払方法、支払合計のカラム名がわかりにくい。
- 支払方法のデータ型がstringになっている。

## Buy detailsテーブル
- buy_idがFKとして存在していない。
