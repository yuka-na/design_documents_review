# テーブル定義書1
## 全体
- テーブル名が大文字になっている。
- カラム名に自テーブル名を入れない。

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

## discs
- テーブル名_* のテーブル名は不要(disk_id => id)

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

## genre
- PKがありません。
- products_idは不要です。

## cart item
- table名にspaceは使えません。スネークケースで作成して下さい。
- PKがありません。
- user_idにauto increment, indexは不要です。
- products_id FKのカラム名は単数形です。データ型が空欄なので、確認下さい。

## buy detail
- table名にspaceは使えません。スネークケースで作成して下さい。
- 商品データは持ちませんか？

## buy
- table名に動詞は使えません。名詞の複数形にして下さい。
- pay stringで持つのは好ましくありません。 enumで調べてみて下さい。
- buy_atの用途不明です。







