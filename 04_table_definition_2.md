# テーブル定義書2
## 全体
- 主キーは~idという命名規則ではなくid
- カラム命名規則(adminテーブルのadmin_emailカラムではなくadminテーブルのemaiカラム)

## users
- l_name,f_name等意味合いを省略して書くとカラムの役割がわかりづらい
- telだけだと用途がわかりづらい
- メンバーステータスの命名規則、ユーザー情報なのに急にメンバーになるのはおかしい

## discs
- disc_num 基本的にカラムの命名は省略けいを使わない

## cart_items
- テーブル名がスネークケースで書かれていない
- Cart item_idはidのみで記述
- buy_numの命名がわかりづらい

## sell_details
- テーブルの命名が不適切、order_detailsとかがいい

## sells
- テーブルの命名が不適切、orderとかがいい