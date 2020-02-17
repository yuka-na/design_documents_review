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
