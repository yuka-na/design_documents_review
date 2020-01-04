# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。


# フィードバック
【フィードバックは消さないこと】
[add]→付け加えなければいけないところ
[fix]→修正が必要なところ
[comment]→その他コメント

## 全体
- ↑ この通りであれば全てのテーブル名を table_id → id
[comment]→その通り！
[add]→　created_atとupdated_atの「カラム説明」が全て「ユーザ」を対象とすることになっている。
- created_atとupdated_at のカラム説明を ユーザ登録日時、更新日時 → 登録日時、更新日時
[add]→　全体的にテーブルとカラムの命名について見直すべき。命名規則は「管理者側での視点」「小文字、アンダーバーで単語を連結させる」「複数、単数形に注意」


## Users
- テーブル名を Users → users
- 名前(性) → 名前(姓)
[comment]→俺も初めて誤字に気がついたw
- DEFAULTがFALSEになっているのでデータ型は string → boolean(またはintegerにして、備考欄にenumで管理を追加)
[fix]→ member_statusという命名だと、何の情報を表しているか、不明確。
- 退会ステータスカラムをstatus, user_statusなどに変更
[add]→　「電話番号」や「郵便番号」のデータ型はintegerにしてしまうと、0始まりの数列の場合、頭の0が取れるからstringで。　
- 電話番号と郵便番号のデータ型を integer → string

## Buy
- テーブル名をBuy → Buys
[fix]→ そもそも、命名規則的にテーブル名に動詞を使うことは不適。名詞にする。また、「管理者側での視点」で命名することを心かける。この場合、購入された商品は管理者側からは「注文」or「受注」と言った表現が適切。
- テーブル名を Buy → orders
- 支払い方法カラムはenumで管理した方が楽(データ型をstring → integer)
[fix]→ payという命名は不適。
- 支払い方法カラムを pay → pay_method
[add]→子テーブル（buy_details）のidをFKとして持っている
- buy_details_id　が不要
[add]→送付先住所はあるが、郵便番号と住所がないのはなぜか？
- 送付先の郵便番号、電話番号、氏名カラムの追加
[add]→stockカラム、命名が不適
- 支払い合計カラムのカラム名 stock → total

## Buy details
- テーブル名をBuy details → Buy_details
[fix]→ buyテーブルと同じ理由で「注文」or「受注」と言った表現に変更する。
- テーブル名を Buy details → order_details
[add]→　スネークケース（アンダーバーで単語を連結すること）が使われていないカラムがある
- 小計金額カラムを subtotal → sub_total
- 購入枚数カラムを buy num → buy_number

## Cart item
- テーブル名をCart item → Cart_items
[fix]→ いや、cart_items。小文字っす
- テーブル名を Cart item → cart_items
[add]→products_idではなく、product_idにすべき
- FKである商品IDのカラム名を products_id → product_id
[add]→小計金額は不要。小計はただの掛け算ですぐ求まる値のため。わざわざデータベースに格納する必要はない。
- 小計金額カラムは不要

## Genre
- テーブル名を Genre → genres
- genreカラムのカラム名をnameやgenre_nameに変更
[fix]→ テーブル名とカラム名に同じ言葉を含めるのはnot good。
- genreカラムのカラム名をnameに変更
[add]→product_idは不要
- product_idは不要(商品テーブルは子であるため)

## Aritists
- テーブル名を Artists → artist
- artistカラムのカラム名をnameやartist_nameに変更
[fix]→ テーブル名とカラム名に同じ言葉を含めるのはnot good。
- artistカラムのカラム名をnameに変更
[add]→product_idは不要
- product_idは不要(商品テーブルは子であるため)

## Labels
- テーブル名を Labels → labels
- labelカラムのカラム名をnameやlabel_nameに変更
[fix]→ テーブル名とカラム名に同じ言葉を含めるのはnot good。
- labelカラムのカラム名をnameやlabel_nameに変更
[add]→product_idは不要
- product_idは不要(商品テーブルは子であるため)


## Products
- テーブル名を Products → products
[add]→cd_titleはtitleで十分。
- シングル/アルバム名 cd_title → title
[add]→FKの記載がない。
-ここはもともと書いてあったこの記述ではダメでしょうか？確認お願いします！(genre_id, label_id, artist_idのFKに○を追加)
[add]→product_という接頭辞はいらない。idで十分。
- product_id → id

## Discs
- テーブル名を Discs → discs
[add]→disc_という接頭辞はいらない。idで十分。
- disc_id → id
[add]→products_idではなく、product_idにすべき。
- products_id → product_id

## Songs
- テーブル名を Songs → songs
- songカラムのカラム名をnameやsong_nameに変更
[fix]→ テーブル名とカラム名に同じ言葉を含めるのはnot good。
- songカラムのカラム名をnameに変更

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
