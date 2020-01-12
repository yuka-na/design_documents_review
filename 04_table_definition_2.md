# テーブル定義書2
## 全体
- table名を同じテーブル内のカラム名に使用しないで下さい。

## users
- カラム名は省略形NGです。(l,f => last_name, first_name)
- カラム説明内[性]で合っていますか？
- userという命名は避けましょう。管理者もuserです。

## ships
- id index持たない理由はありますか？
- name 姓名分けなくて良いのでしょうか？フリガナは？

## discs
- FK 単数形です。

## cart items
- table名にspaceは使えません。スネークケースで作成して下さい。
- FK 単数形です。

## sell_details
- products_id はFKではないのでしょうか？
- FK 単数形です。

## sells 
- table名に動詞は使えません。
- FK 単数形です。
- tax管理は不要でしょうか？


**研修担当レビュー**
<font color="Red">再提出の際はこのレビューを残しておいてください。</font>

## 全体
- Railsでテーブルを作成した際のPKの命名は合っていますか？

## admins
- PKにindexが付与されていませんが問題ありませんか？

## users
- memeber_statusカラムがありますが、このカラムの命名は問題ありませんか？

## ships
- > name 姓名分けなくて良いのでしょうか？フリガナは？

  とありますが、特に要件にないのでこの指摘は不要です

## products
- stockカラムは必要でしょうか？
- stock_statusカラムは必要でしょうか？

## cart items
- `buy num`カラムはテーブル名と同様に空白を含めることはできないので命名が不適切です

## sell_details
- 価格はどのように管理しますか？
- 親モデル(sell)の外部キーは必要ありませんか？

## sells
- 子モデル(sell_details)の外部キーは必要でしょうか？
- totalカラムがありますが、この命名はどのような値が入るか明確でしょうか？
