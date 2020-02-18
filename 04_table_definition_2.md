# テーブル定義書2

## adminsテーブル
- カラム名にadminという接頭辞は必要ない。

## usersテーブル
- user_l_name,user_f_nameではなにを示しているかわからない。
- カラム名にuserという接頭辞は必要ない。
- member_statusのデータ型がinteger/enumとなっている。true,falseで管理するなら、boolean形にすべき。またその際はenumを使う必要がない。

## shipsテーブル
- カラム名にshipという接頭辞は必要ない。

## productsテーブル
- products_idになっている。命名規則的にproduct_idにすべき。
- ジャケット画像にrefileを使うのなら、備考欄に記述すべき。

## songs,labels,artists,genresテーブル（共通）
- ～名のカラム名は~_nameという風にわかりやすい名前にすべき。

## cart itemsテーブル
- cart itemsではなくcart_itemsにすべき。
- カラム名が大文字になっている。
- 購入枚数ではなく、数量にすべき。quantityなどが望ましい。

## sell_detailsテーブル
- 商品IDのFK漏れ
- 購入時価格のカラムがない。

## sellsテーブル
- 購入詳細IDを持っている。これではこちらが多になってしまう。
- 支払い方法、支払い合計はもっとわかりやすい名前にすべき。


# フィードバック
[add]→付け加えなければいけないところ
[fix]→修正が必要なところ
[comment]→その他コメント（修正ではないけど、確認して欲しいポイントです）

## 全体
- [add]各テーブルにidというカラムがない。（テーブル名_idという名前だと不適切）

## admins
- admin_id(id)にindexがない。

## users
- [fix]members_statusはinteger/enumで問題ありません。member_statusのステータスは、何を意味しているでしょうか？

## ships
- [add] ship_idにindexがない。

## products
- [add] stockは入荷と売上履歴から算出できるので不要です。
- [add] stock_statusはstockの個数から判別できるので同じく不要。
- [add] ジャケット画像のデフォルト値への言及をお願いします。

## discs
- [add] disc_numのdisc_は不要。
- [add] products_idは単数形なのでproduct_idにする。productが親です。

## sell
- [add] totalについて詳しい説明をお願い致します。
