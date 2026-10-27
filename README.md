# discordOGP

Discord で URL を貼ったときに表示される OGP カード用の静的 HTML テンプレートです。

## 使い方

1. `index.html` を開く
2. `<head>` 内の以下を編集する
   - `og:title`
   - `og:description`
   - `og:image`
   - `og:site_name`
   - `theme-color`
3. そのまま GitHub Pages または静的ホスティングに配置する
4. Discord に URL を貼って表示を確認する

## 例

- タイトルの変更: `meta property="og:title" content="ここにタイトル"`
- 説明の変更: `meta property="og:description" content="ここに説明文"`
- 画像の変更: `meta property="og:image" content="https://example.com/image.png"`

## GitHub Pages で公開する場合

- GitHub リポジトリの Settings → Pages を開く
- Source を `Deploy from a branch` に設定
- Branch を `main`、Folder を `/root` にする
- 公開URLは `https://<ユーザー名>.github.io/discordOGP/` の形式になります

## メモ

- Discord はティザー取得のため、`https://` の完全なURLが必要です
- `og:image` は必須ではありませんが、あるとカードの見栄えが良くなります
- 画像は HTTPS の公開URLを指定してください
