# Next.js + FastAPI Project

このプロジェクトは、Next.jsをフロントエンド、FastAPIをバックエンドとして使用する現代的なWebアプリケーションです。

## 技術スタック

### フロントエンド
- **Next.js** - Reactベースのフロントエンドフレームワーク
- TypeScript - 型安全な開発環境
- TailwindCSS - スタイリング
- Axios - HTTP クライアント

### バックエンド
- **FastAPI** - 高性能なPython製Webフレームワーク
- Python 3.9+
- SQLAlchemy - ORMマッパー
- Pydantic - データバリデーション
- PostgreSQL - データベース

## プロジェクトの構造

```
.
├── frontend/               # Next.jsプロジェクト
│   ├── src/
│   │   ├── components/    # 再利用可能なコンポーネント
│   │   ├── pages/        # ページコンポーネント
│   │   ├── styles/       # スタイルファイル
│   │   └── utils/        # ユーティリティ関数
│   ├── public/           # 静的ファイル
│   └── package.json
│
└── backend/               # FastAPIプロジェクト
    ├── app/
    │   ├── api/          # APIエンドポイント
    │   ├── core/         # 設定ファイル
    │   ├── models/       # データベースモデル
    │   └── schemas/      # Pydanticモデル
    ├── tests/            # テストファイル
    └── requirements.txt
```

## 開発環境のセットアップ

### フロントエンド

```bash
# フロントエンドのセットアップ
cd frontend
npm install
npm run dev
```

### バックエンド

```bash
# 仮想環境の作成と有効化
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 依存関係のインストール
cd backend
pip install -r requirements.txt

# 開発サーバーの起動
uvicorn app.main:app --reload
```

## 主な機能

- 🔐 JWT認証
- 🚀 REST API
- 📦 データベース統合
- 🔄 リアルタイムデータ更新
- 📱 レスポンシブデザイン

## API ドキュメント

APIドキュメントは以下のURLで確認できます：
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## 環境変数

### フロントエンド (.env.local)
```
NEXT_PUBLIC_API_URL=http://localhost:8000
```

### バックエンド (.env)
```
DATABASE_URL=postgresql://user:password@localhost/dbname
SECRET_KEY=your-secret-key
```

## デプロイ

- フロントエンド: Vercel推奨
- バックエンド: Heroku, AWS, GCP等に対応

## ライセンス

MIT

## コントリビューション

1. このリポジトリをフォーク
2. 新しいブランチを作成 (`git checkout -b feature/awesome-feature`)
3. 変更をコミット (`git commit -am 'Add awesome feature'`)
4. ブランチにプッシュ (`git push origin feature/awesome-feature`)
5. プルリクエストを作成