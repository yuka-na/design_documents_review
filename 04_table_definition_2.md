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
