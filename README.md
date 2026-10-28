# discordOGP

Discord でカードを表示したいときに使う OGP 生成ページです。

## 使い方

1. `index.html` を開く
2. タイトル・説明・画像URLを入力する
3. `URLを生成` を押す
4. 表示されたURLを Discord に貼る

生成された URL は `card.html` を指していて、Discord に貼ると OGP カードが表示されます。

例:

https://roburuchan-blip.github.io/discordOGP/card.html?t=%E4%BB%8A%E6%97%A5%E3%81%AE%E5%91%8A%E7%9F%A5&d=20%E6%99%82%E3%81%8B%E3%82%89%E9%85%8D%E4%BF%A1%E3%81%97%E3%81%BE%E3%81%99&c=5865f2

## GitHub Pages で公開する方法

1. GitHub のリポジトリで `Settings` → `Pages` を開く
2. `Deploy from a branch` を選ぶ
3. `main` / `/root` を選択
4. 公開 URL が発行される

## 補足

- 画像URL は `https://` を使う
- Discord はキャッシュを持つため、最初に反映されない��きは URL の末尾に `&v=1` を付けて確認してください
- `card.html` は OGP 用のページであり、ここに `meta property="og:title"` などが埋め込まれます
