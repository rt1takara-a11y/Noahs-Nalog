# Noah's Nalog — Web サイト

小規模事業者・飲食店向けプロダクト「Noah's Nalog（マニュアル）」と「LogMate（AI経営ログ）」の
ポータルサイトと各プロダクトLPです。静的HTMLのみ（外部依存なし・単一ファイル構成）。

## 構成

```
/
├── index.html        トップ（ポータル：2プロダクトへの導線）
├── manual/index.html Noah's Nalog マニュアル LP
└── logmate/index.html LogMate LP
```

- 全ページ、外部CDN・フォント・スクリプトへの依存なし。1ファイルで完結。
- ライト / ダーク両テーマ対応（OS設定に追従＋右上ボタンで切替）。
- ページ間リンクはすべて相対パス。サブパス配信（GitHub Pages のプロジェクトサイト等）でもそのまま動作。

## ローカルで確認

```bash
python3 -m http.server 8000
# http://localhost:8000/ を開く
```

## デプロイ

リポジトリのルートをそのまま公開すれば動作します。

- **GitHub Pages**: Settings → Pages → Deploy from a branch → `main` / `/ (root)`
- **Cloudflare Pages / Netlify / Vercel**: ビルドコマンドなし、公開ディレクトリはルート

## メモ

- マニュアルLPの「はじめる / アプリを開く」は本番アプリ（Cloudflare Workers）へリンクしています。
- LogMate LP・トップの問い合わせCTAは `mailto:` です。運用に合わせて申込フォーム等へ差し替えてください。
