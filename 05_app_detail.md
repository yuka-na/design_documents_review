# アプリケーション詳細設計
## 全体
- トップページはどのアクションでしょうか？
- endとadminが同じurlを使うことはできません。
  adminは"/admin/?"のような切り分けをお願いします。
- device等で自動生成されたpathも記載お願いします。
- urlの単数形複数形の使い分けがない。 基本index以外は複数

## users
- createがありません。 sign_upできません。
- userの退会確認ページ・完了ページのpathがありません。

## cds
- editに対するワイヤーフレームがありません。

## addresses
- indexありませんが、宛先一覧は作らないでよいのでしょうか？
- new必要でしょうか？
- edit/update/destroyにadminのpathを追加して下さい。

## cart_item 
- editは必要でしょうか？

## orders
- urlが重複しています。

## admins
- showがトップページであっていますか？
- edit/showでURLが重複しています。







