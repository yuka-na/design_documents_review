# 設計レビュー最終課題README
## やること
- 以下のレビュー対象の設計書について、レビューを行ってもらいます。
- **修了試験は2段階に分かれています。**
  - 1段階は**問題抽出**。
    - 対象の設計書について、添付している**markdownファイル**に、問題点を列挙してください。
    - 形式は、テンプレートの形を守ってください。
   - 2段階は**レビュー文章化**。
      - **問題抽出に合格してから取り組んでください。**
      - 1段階で提出した問題点について、要件に従う形にしてもらえるようレビュー文章を作成してください。
      - 形式は課題に対して、引用する書き方にしてください。


### レビュー形式例
```
## エンドユーザ
- 論理削除を考慮していない。（問題点）
  > ユーザを削除した場合、該当のレコードはどうなりますか？（レビュー）
```

## 準備(リポジトリのfork)
- このリポジトリをforkし、自分のアカウントで使うリポジトリを作成してください。

## 提出方法
- 設計図に対する問題点/レビューを該当するmarkdownファイルに記載してください。
- 問題抽出では、**１つの設計書を問題抽出するごと**に提出してください。
- レビュー文章化では、**全ての設計書をまとめて**提出してください。
- branchは**master**で行ってください。
- commit messageは`問題抽出_xxx_n回目`, `レビュー_n回目`としてください。
    - xxxは設計書の種類。
- 提出するときはfork先のリポジトリURLを[フォーム](https://forms.gle/DXSfWbYKxQH3hegG9)から提出してください。



## 研修担当からのレビュー
- 提出してもらったGithubリポジトリに対して、Pull Requestとしてレビューが飛んできます。
- **合格するまで**は、そのレビューを踏まえて修正を行い、再度[フォーム](https://forms.gle/DXSfWbYKxQH3hegG9)から提出をお願いします。



## レビュー対象の設計書
### データベース設計
- ER図
  - 01 : https://drive.google.com/open?id=1vmMD2q76GOOmyuhuzgkJsk9nRcNhoOhE
  - 02 : https://drive.google.com/open?id=1iYVDuKeXzSM7Cq7bpXXR_SNu_qqxmdx0
- テーブル定義書
  - 01 : https://drive.google.com/open?id=1wZb6VJ-R-l7HDswsxH76Y3_ZXx07vZUyJ4wwFFI2Svk
  - 02 : https://drive.google.com/open?id=1jx9q22FS50O2qUz0miKJvt-gflGKFfcrrZ9Ubu_z9_g
  
### アプリケーション詳細設計
- 設計書 : https://drive.google.com/open?id=1EWayigGHKoqL_wm6fKodic7vaE5BXuxsSa5LM8GOUQc
- 参考ワイヤーフレーム : https://drive.google.com/open?id=1Zurk2OCDyitQuVNZcFHkeaxf-RXEdYrf
