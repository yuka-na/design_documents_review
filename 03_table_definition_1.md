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



# フィードバック
[add]→付け加えなければいけないところ
[fix]→修正が必要なところ
[comment]→その他コメント（修正ではないけど、確認して欲しいポイントです）

## 全体
- [add]→各テーブルのcreated_upとupdated_atを再確認してください！
- [add]→テーブル名は小文字かつ複数形
- [add]→テーブル名とカラム名に同じワードを含めない
- [add]→AUTOINCREMENTとINDEXが抜けている箇所がある

## Adminテーブル
- [add]→deviseで作るパスワードカラムとemailカラムの名前ってなんでしたっけ？

## Usersテーブル
- [add]→配送先カラムがあるが、複数の配送先情報を保管することが考慮できていない

## Productsテーブル
- [add]→在庫数ステータスカラムについて
- [add]→在庫数カラムについて

## Artistsテーブル
- [add]→子要素のidを持ってしまっている

## Genreテーブル
- [add]→子要素のidを持ってしまっている

## Buy,Buy detailsテーブル(共通)
- [add]→buy,buy_detailは管理者視点の命名になっていない

## Buyテーブル
- [add]→payカラムについて
- [add]→送付先住所はあるが、郵便番号と住所がない。

## Buy detailsテーブル
- buy_idがFKとして存在していない。

## [add]discs,songs,labels,cart_itemについても指摘事項があるので追記しましょう
