# Scale

司法試験・予備試験の学習を、もくもく続けるための記録アプリ。
学習時間を科目ごとに記録し、**科目バランス**・**過去問の進み具合**・**連続日数**をひと目で。今日／今週のまとめは **X にシェア** できます。

- ビルド不要・1ファイル完結（`index.html` + `manifest.json` + `sw.js`）
- 記録はすべて端末内（localStorage キー `scale_v1`）。広告・追跡・ログインなし。オフライン対応（PWA）
- 初期科目は予備試験ベース（憲・行・民・商・民訴・刑・刑訴・実務基礎・選択）。自由に追加／編集／並び替え可能
- ストップウォッチ計測、種類タグ（論文／短答／インプット／実務）、週の目標時間、過去問カウンタ
- X シェアは投稿用テキストを作って共有するだけ（自動投稿はしません）

## アイコンの作り直し

```sh
convert -background none icons/icon.svg -resize 192x192 icons/icon-192.png
convert -background none icons/icon.svg -resize 512x512 icons/icon-512.png
```

## デプロイ（Cloudflare Pages）

1. このリポジトリを Cloudflare Pages に接続
2. ビルド設定：フレームワークなし／ビルドコマンド空欄／出力ディレクトリ `/`
3. カスタムドメイン（例：`scale.xdcyw.net`）を割り当て

© 2026 田中志

## アップデート履歴

## 2026-06-16
- OGタグ追加（og:title / og:description / og:image / og:url / og:type / twitter:card）
- キーボードアクセシビリティ改善（:focus-visible スタイル追加）
- manifest.json 整備（scope・categories・orientation 修正）
