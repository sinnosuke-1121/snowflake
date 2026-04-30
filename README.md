# Snowflake SnowPro Core 苦手復習クイズ - PWA

模擬試験1〜4の不正解問題194問を反復学習できるWebアプリ。
GitHub Pagesにデプロイし、iPhoneのSafariで「ホーム画面に追加」すると
ネイティブアプリのように使えます(オフラインも対応)。

## 📱 iPhoneにインストールする手順

### 1. GitHubにアップロード

1. GitHub.comにログイン
2. 右上の「+」→「New repository」
3. **Repository name**: 好きな名前(例: `snowpro-quiz`)
4. **Public**を選択(無料のGitHub PagesはPublicリポジトリのみ)
5. 「Create repository」をクリック
6. 「uploading an existing file」をクリック
7. このフォルダ内の **すべてのファイル**(`index.html`, `bundle.js`, `manifest.json`, `sw.js`, `icon-*.png`, `README.md`)をドラッグ&ドロップ
8. 「Commit changes」をクリック

### 2. GitHub Pagesを有効化

1. リポジトリの **Settings** タブを開く
2. 左サイドバーの **Pages** をクリック
3. **Source** セクションで:
   - Branch: `main`(または `master`)
   - Folder: `/ (root)`
4. **Save** をクリック
5. 数分待つと、ページの上部に
   `Your site is live at https://<ユーザー名>.github.io/<リポジトリ名>/`
   と表示されます

### 3. iPhoneのSafariでインストール

1. iPhoneの **Safari** を開く(Chromeなど他ブラウザではPWA機能が制限される)
2. 上記のURLにアクセス
3. アプリが正しく表示されることを確認
4. 画面下の **共有ボタン**(↑のついた四角)をタップ
5. **「ホーム画面に追加」** をタップ
6. 名前を確認して **「追加」** をタップ
7. ホーム画面に雪の結晶アイコンが追加されます

これで完了。アイコンをタップするとフルスクリーンで起動します。

## ✨ 機能

- 194問の不正解問題を全網羅(模擬試験1〜4)
- 模擬試験(M1〜M4) × ドメインで絞り込み
- クイズモード(シャッフル + 即時解説)
- レビューモード(全問解説確認)
- 自分で問題を追加可能
- 進捗(正解数・正解率)はIndexedDBに保存
- オフライン対応(初回読み込み後はネット不要)

## 📝 データの保存場所

進捗データと自作問題は、iPhoneのSafari/PWA内のIndexedDBに保存されます。
**Safariの設定でWebサイトデータを削除するとリセットされる**点に注意。

## 🔧 アプリを更新するには

修正したファイルをGitHubに再アップロードすれば、
PWAも自動でキャッシュ更新されます(数秒〜数分)。
