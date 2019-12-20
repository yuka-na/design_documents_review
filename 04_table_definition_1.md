# テーブル定義書1
## 全体
- Genres, Artists, Labels, Songs, AdminsテーブルにPKがない
- 自分以外の住所を格納する場所がない

## Users
- user_f_name, user_f_kanaにNOT NULLがかかっていない
- 名前(性) → 名前(姓)

## Buy
- 購入日カラムが不要
- テーブル名をBuy → Buys
- 配送ステータスがない

## Buy details
- テーブル名をBuy details → Buy_details

## Cart item
- テーブル名をCart item → Cart_items
- カラム名をbuy num → buy_number

## Genre
- テーブル名をGenre → Genres

## Admin
- テーブル名をAdmin → Admins

## Products
- カラム名をnotax_price → no_tax_price

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
