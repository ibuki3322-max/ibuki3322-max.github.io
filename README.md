# アプリ掲載情報の更新

`data/apps.json` がトップページと「みんなで遊ぶ」ページの掲載情報の元データです。
アプリの追加・削除、名前、アイコン、App Store URL、公開日をここで編集してください。
ゲームページにも載せる作品には `multiplayer` を設定します。`order` が表示順、`modes` が絞り込み項目です。
公式サイトがある作品は `officialUrl`、Androidテスター募集の案内ページがある作品は `androidTestUrl` を設定します。

編集後、プロジェクトのルートで次を実行します。

```sh
python3 scripts/build_site.py
```

このコマンドで `assets/apps-data.js`、トップページの作品カードと件数、「みんなで遊ぶ」のゲームカードと件数、`sitemap.xml` と `robots.txt` を更新します。アプリ詳細ページは別途編集してください。

ヒーロー画像は `assets/*-hero.webp` を表示に使います。元のPNGは編集用に残しています。
