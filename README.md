# ゼロチェック LP（静的1枚）

このフォルダは、1ページ完結の静的LPテンプレです。
- 会社名: ゼロチェック
- ロゴ: assets/logo.png（添付ロゴを配置済み）

## ローカルで表示

### 方法A：そのまま開く
index.html をブラウザで開けばOKです。

### 方法B：ローカルサーバ（おすすめ）

```bash
cd zero-check-lp
python -m http.server 8080
```

http://localhost:8080 を開いてください。

## 公開（静的ホスティング）

### Cloudflare Pages
- New project -> Upload assets
- Framework preset: None
- Build command: なし
- Output directory: ルート

### Vercel
- New project -> Import
- Framework preset: Other
- Build command: なし
- Output: ルート

## 差し替えポイント

index.html 冒頭の const SITE 設定だけ触ればほぼ完了です。
- companyName / phone / hours / lineUrl
- formEndpoint（フォーム送信先）

画像を差し替える場合は assets 以下を置き換えてください。

## フォーム送信

デフォルトは「送信しました（デモ）」の挙動です。
本番では SITE.formEndpoint を自前APIやフォームサービスに向けてください。
