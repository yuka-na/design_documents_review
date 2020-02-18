# テーブル定義書1
## 全体
- 主キーになるカラムはidでよい。
- テーブル名はすべて小文字かつ、複数形。
- created_at,updated_atがすべてユーザ登録日時、更新日時になっている。
- Songs,Labels,Artists,Genre,Cart itemテーブルに主キーがない。
- deviseを使う場合は備考にdeviseと追記。
- AUTOINCREMENTとINDEXが抜けている箇所がある。（主キーに追記）
- テーブル名とカラム名に同じ名前を含めてはならない。

## Adminテーブル
- 管理者IDのPK漏れ
- 管理者IDのAUTOINCREMENTが抜けている。
- deviseのデフォルトではメールアドレスはemail, パスワードはencrypted_password

## Usersテーブル
- user_l,user_fではなにを示しているかわからない。
- 名前（名、名カナ）にNOT NULL がついていない。
- 郵便番号はstring型であるべき。
- 電話番号も同様。
- user_~というuser_の接頭辞は必要ない。
- member_statusのデータ型がstringになっている。
- 配送先住所について、複数の配送先があることを考慮していない。
- deviseのデフォルトではメールアドレスはemail, パスワードはencrypted_password

## Productsテーブル
- disc_idがある。
- genre_id,label_id,artist_idのFK漏れ
- products_idというように複数形になってしまっている。
- 入荷による在庫管理ができない。入荷テーブルを作るべき。
- 在庫ステータスのデータ型がstringになっている。

## Discsテーブル
- トラックNoではなく、ディスクNoにすべき。

## Songsテーブル
- 曲順の管理を考慮していない。

## Cart itemテーブル
- 小計金額は計算で求められるので、必要ない。
- 購入枚数ではなく数量にすべき。quantityなど

## Artists,Genre,Cart item,Songsテーブル(共通)
- FKにAUTOINCREMENTがついている。

## Artists,Genre,labelsテーブル(共通)
- 子要素のid(products_id)を持っている。

## Artistsテーブル
- アーティスト名がinteger型になっている。

## Genreテーブル
- ジャンル名がinteger型になっている。

## Buy,Buy detailsテーブル(共通)
- buy num -> buy_num
- 管理者視点のテーブル名にすべき。ordersなど

## Buyテーブル
- buy_details_idは必要ない。
- 支払方法、支払合計のカラム名が説明と合っていない。
- 支払方法のデータ型がstringになっている。
- 郵便番号と住所がない。

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
