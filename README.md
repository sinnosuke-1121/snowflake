# Snowflake SnowPro Core 認定試験 + SQL学習 - PWA

Snowflake学習用Webアプリ。
**2つのモードを切り替えて使えます:**
- **認定試験対策**: 模擬試験1〜4の不正解問題194問
- **SQL学習**: Snowflake頻出SQL構文65問(覚え方フレーズ + 使われ方付き)

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
7. このフォルダ内の **すべてのファイル**をドラッグ&ドロップ
8. 「Commit changes」をクリック

### 2. GitHub Pagesを有効化

1. リポジトリの **Settings** タブ → **Pages**
2. **Source**: Branch=`main`、Folder=`/ (root)` → **Save**
3. 数分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` が公開されます

### 3. iPhoneのSafariでインストール

1. SafariでURLにアクセス
2. 共有ボタン → **「ホーム画面に追加」** → **追加**

## ✨ 機能

### 認定試験対策モード
- 模擬試験1〜4で誤答した194問を反復学習
- 模擬試験(M1〜M4) × ドメインで絞り込み
- 自分で問題を追加可能

### SQL学習モード
- Snowflake頻出SQL 65問(15カテゴリ)
- 各問題に「使われ方」と「覚え方フレーズ」付き
- カテゴリ × ドメインで絞り込み
- カテゴリ例: Warehouse / Database & Schema / Table / Time Travel / Data Loading / Stream / Task / Sharing / Roles & Permissions / Snowflake Functions / DML など

### 共通機能
- クイズの中断と再開(続きから始められる)
- 進捗(正解数・正解率)の永続保存
- オフライン対応

## 📝 データの保存場所

進捗データ・自作問題・中断中のクイズセッションは、iPhoneのSafari/PWA内のIndexedDBに保存されます。
**Safariの設定でWebサイトデータを削除するとリセットされる**点に注意。

## 🔧 アプリを更新するには

修正したファイルをGitHubに再アップすればPWAも自動でキャッシュ更新されます。
