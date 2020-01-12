# テーブル定義書1
## 全体
- テーブル名が大文字になっている。
- カラム名に自テーブル名を入れない。
- created_atが全てユーザ登録日時になっている。
- updated_atが全てユーザ更新日時になっている。
- member_statusが何を意味しているか不明。

## admins
- テーブル名は複数形がデファクト。
- PKが抜けている。
- [テーブル名_*]のテーブル名は不要
- id のindex,auto incrementが抜けている。

## users
- テーブル名_* のテーブル名は不要
- 姓名のカラム名が分かりづらい。(l,f => last_name, first_name)
- カラム説明内[性]で合っていますか？
- 名前のNOT NULLが○でないのには理由がありますか？
- zip_code データ型不適合。[001-0000]に送りたい場合、うまくいきますか？電卓などで入力してみて下さい。
- telもzip-codeと同様。[09001234567]等
- ship_addressは別テーブルを作成して下さい。
- member-statusのデータ型不適合。stringで文字で管理するのは手間。0or1のデータ型を調べてみて下さい。

## products
- テーブル名_* のテーブル名は不要
- disc_idは不要
- genre_id FKではないでしょうか？
- lable_id FKではないでしょうか？
- artist_id FKではないでしょうか？
- label_id FKではないでしょうか？
- image stringではダメでしょうか？ [cd_]は必要ですか？
- title [cd_]は必要でしょうか？
- 在庫状況をステータス管理しているので、在庫数と食い違う可能性がある。
- 在庫数カラムがある（入荷と売上から算出できる）。

## discs
- テーブル名_* のテーブル名は不要(disk_id => id)
- products_idではなく、product_idにすべき。
- track_noの用途が不明。
- 複数枚組を考慮してない

## songs
- PKがありません。
- song のデータ型はintegerで良いのでしょうか？
- disc_id auto increment は不要です。

## labels
- PKがありません。
- products_idは不要です。

## artists
- PKがありません。
- products_idは不要です。
- artistカラムがアーティスト名をもつならばnameなどとするべき。
- artistカラムが曲名をもたせるのに、integerとなってる。

## genre
- PKがありません。
- products_idは不要です。
- genreカラムがアーティスト名をもつならばnameなどとするべき。
- genreカラムが曲名をもたせるのに、integerとなってる。

## cart item
- table名にspaceは使えません。スネークケースで作成して下さい。
- PKがありません。
- user_idにauto increment, indexは不要です。
- products_id FKのカラム名は単数形です。データ型が空欄なので、確認下さい。
- buy numの意味が不明。_(アンダースコア)をつけてない。
- 小計金額は不要（数量と商品の価格から算出可能）。

## buy detail
- table名にspaceは使えません。スネークケースで作成して下さい。
- 商品データは持ちませんか？
- buy detailsだと受注詳細の意味にならない。

## buy
- table名に動詞は使えません。名詞の複数形にして下さい。
- pay stringで持つのは好ましくありません。 enumで調べてみて下さい。
- buy_atの用途不明です。
- buyだと受注の意味じゃない。
- 子テーブル（buy_details）のidをFKとして持っている。
- payが何を意味しているか不明。
- 支払合計がstockになっていて意味不明。
- 送付先住所はあるが、郵便番号と住所がない。


**研修担当レビュー**
<font color="Red">再提出の際はこのレビューを残しておいてください。</font>

## 共通
- created_atが全てユーザ登録日時になっている。
- updated_atが全てユーザ更新日時になっている。
- member_statusが何を意味しているか不明。

## Products
- 在庫状況をステータス管理しているので、在庫数と食い違う可能性がある。
- 在庫数カラムがある（入荷と売上から算出できる）。

## Discs
- products_idではなく、product_idにすべき。
- track_noの用途が不明。
- 複数枚組を考慮してない

## Artists
- artistカラムがアーティスト名をもつならばnameなどとするべき。
- artistカラムが曲名をもたせるのに、integerとなってる。

## Genre
- genreカラムがアーティスト名をもつならばnameなどとするべき。
- genreカラムが曲名をもたせるのに、integerとなってる。

## Cart item
- buy numの意味が不明。_(アンダースコア)をつけてない。
- 小計金額は不要（数量と商品の価格から算出可能）。

## buy
- buyだと受注の意味じゃない。
- 子テーブル（buy_details）のidをFKとして持っている。
- payが何を意味しているか不明。
- 支払合計がstockになっていて意味不明。
- 送付先住所はあるが、郵便番号と住所がない。

## Buy details
- buy detailsだと受注詳細の意味にならない。
