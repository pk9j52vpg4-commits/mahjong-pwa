# 麻雀収支管理アプリ — iPhone用PWA

## ファイル
- index.html: 画面
- style.css: デザイン
- app.js: 記録、集計、編集、バックアップ、グラフ
- manifest.webmanifest: ホーム画面アプリ設定
- sw.js: オフライン用キャッシュ
- icon-192.png / icon-512.png / apple-touch-icon.png: アイコン
- .nojekyll: GitHub Pages用

## iPhoneからGitHub Pagesで公開
1. Safariで github.com にログインし、New repository を押す。
2. Repository name を `mahjong-pwa`、Public を選び、Create repository。
3. Add file → Upload files からこのフォルダ内のファイルを**ZIPではなく展開した状態で**アップロードする。iPhoneの「ファイル」アプリでZIPをタップすると展開できる。
4. Commit changes を押す。
5. Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main → /(root) → Save。
6. Pagesに表示されるURLをSafariで開く。通常は https://ユーザー名.github.io/mahjong-pwa/ となる。
7. Safariの共有ボタン → ホーム画面に追加 → Webアプリとして開くをオン → 追加。

## 注意
- 保存データは端末のブラウザ内のlocalStorage。別端末には自動同期されない。定期的にJSONバックアップを取る。
- Safariとホーム画面アプリで保存領域が異なる場合がある。移行にはJSONバックアップ/復元を利用する。
- 古いHTML版で使用した `mahjong-record-v2` と同じ保存キーを使うが、**公開URLが異なると自動でデータ移行されない**。
- アプリ名は麻雀収支管理アプリだが、現段階ではポイント記録中心。現金収支・広告・プレミアム課金は未実装。
- GitHub Pagesの公開サイトは原則誰でもアクセスできる。コードに個人情報や秘密鍵を含めない。
