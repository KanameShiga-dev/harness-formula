# GitHub Pages 公開手順

## 公開までの5ステップ

1. GitHubで新しいリポジトリを作成します（例：`harness-formula`）。GitHub Freeの場合は公開リポジトリを使用します。
2. このZIPを解凍し、**ZIP内のファイルをすべてリポジトリの最上位階層に**アップロードしてコミットします。`index.html` がリポジトリ直下にあることを確認します（親フォルダを丸ごと1階層深く置かないこと）。
3. リポジトリの **Settings → Pages** を開きます。
4. **Build and deployment → Source: Deploy from a branch**、**Branch: `main` / `(root)`** を選んで保存します。既定のブランチが `main` 以外ならそのブランチを選びます。
5. Pages画面に表示される公開URLを開いて、タイトル→チーム→案件→クイズ10問→走行リプレイ→振り返りを確認します。

一般的なプロジェクトリポジトリのURL形は `https://<ユーザー名>.github.io/<リポジトリ名>/` ですが、正確なURLはGitHubのPages画面で確認してください。

## 含まれるファイル

```text
index.html             ゲーム本体（HTML/CSS/JavaScript内蔵）
README.md              概要（GitHubリポジトリの説明文）
DEPLOY.md              公開手順
HOW_TO_PLAY.md         操作方法と遊び方
PRIVACY.md             データ保存と外部通信について
favicon.svg            ブラウザタブのアイコン
.nojekyll              Jekyllの変換処理を無効化
.gitignore             不要ファイルのGit登録を抑制
assets/                README用スクリーンショット
```

## 確認ポイント

- `index.html` を開いたとき404にならない。
- 画面の「戻る」・「タイトルへ」が動く。
- 8架空チーム、10コースを選べる。
- 問題数が毎回10問で、再挑戦で出題が変わる。
- 05俯瞰2D、06車載視点とチェックポイント助言が見られる。
- 全10コース未達成時にX投稿ボタンが表示されない。
- 記録は同じブラウザ・同じ公開URLで再訪した時に残る（プライベートブラウズ、保存禁止設定を除く）。

## よくある注意点

- **アクセス権**：GitHub Pagesで公開したページはインターネットから閲覧できるため、機密資料や実業務のデータをアップロードしないでください。
- **既存記録の移行**：`file://` で遊んだ記録や別URLの記録は、GitHub Pages上の記録へ自動移行しません。
- **Xへのリンク**：全制覇時はXの投稿作成画面を新規タブで開きます。投稿には本人の操作が必要です。Xログインやブラウザ設定によっては開けないことがあります。その場合はゲーム内のコピー機能を利用してください。
- **プレビュー画像**：README内のスクリーンショットはゲーム内では読み込まれません。ゲーム自体は `index.html` だけで動作します。
- **SNSカード画像**：この版では公開URLが未確定のため `og:image` を付けていません。共有サムネイルを出したい場合は公開後に絶対HTTPS URLで指定してください。
- **利用条件**：OSSライセンスはこのパッケージに同梱していません。必要に応じて利用条件を明確にしてください。

## 公式ガイド

- [GitHub Pages の公開元設定](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Pages のサイト作成](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

公開操作自体はこのパッケージの作成時点では行っていません。
