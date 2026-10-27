# discordOGP

Discord の OGP カードを簡単に作れる静的 HTML ジェネレーターです。

## これができること

- タイトル
- 説明文
- 画像URL
- サイト名
- カラーテーマ

を入力して、Discord に貼ったときに見える HTML を生成できます。

## 重要な注意

Discord は JavaScript を実行しません。
そのため、OGP のカードは `meta property="og:title"` や `meta property="og:description"` などの静的な HTML を見て作ります。

つまり、URL のクエリパラメータだけで動的にOGPを変える方法は、GitHub Pages の通常の静的サイトでは正しく動きません。

正しい使い方は次の通りです。

1. `index.html` を開く
2. フォームに内容を入力する
3. 「HTMLをダウンロード」を押す
4. 生成された `index.html` を公開用の静的サイトに置く
5. Discord にその URL を貼る

## GitHub Pages で公開する方法

1. GitHub リポジトリを開く
2. Settings → Pages を開く
3. Source を `Deploy from a branch` にする
4. Branch を `main`、Folder を `/root` にする
5. 公開URLが表示される

例:

https://roburuchan-blip.github.io/discordOGP/

## 生成される HTML の例

生成した `index.html` には次のような OGP タグが入ります。

```html
<meta property="og:title" content="今日の告知">
<meta property="og:description" content="20時から配信します！">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:site_name" content="マイページ">
<meta name="theme-color" content="#5865f2">
```

## 補足

- 画像URL は `https://` である必要があります。
- 画像がない場合でもタイトルと説明だけで動作します。
- Discord はキャッシュを持つため、反映されないときは URL に `?v=1` のようなクエリをつけて確認してください。
