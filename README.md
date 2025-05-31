# Coconala Marp プレゼンテーションテンプレート

このテンプレートは、[Marp](https://marp.app/)を使用してCoconalaブランドのプレゼンテーションを作成するためのテンプレートです。

## 🎨 特徴

- **Coconalaブランドカラー**: 6色の章別カラーシステム
- **章システム**: 各章2ページ構成（intro + page）の自動化システム
- **三角形アイコン**: CSS疑似要素による自動生成
- **日本語対応**: M PLUS 1pフォントで最適化
- **レスポンシブレイアウト**: 複数のコンテンツレイアウトパターン
- **クロージングページ**: 専用の感謝・連絡先ページ

## 📁 ファイル構成

```
./
├── coconala-presentation.md        # メインテンプレートファイル
├── coconala-theme/
│   ├── coconala-pop.css           # カスタムMarpテーマ
│   └── assets/
│       ├── fonts/M_PLUS_1p/       # 日本語フォント
│       └── images/                # SVG アセット
│           ├── triangle-with-1.svg ~ triangle-with-6.svg
│           ├── title_bg.svg, agenda_bg.svg
│           ├── chapter_1_bg.svg ~ chapter_6_bg.svg
│           └── closing_page_bg.svg
└── README.md                      # このファイル
```

## 🚀 クイックスタート

### 1. Dockerを使用（推奨）

**PDF生成：**
```bash
docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --pdf coconala-presentation.md --allow-local-files
```

**開発時のプレビュー（PNG生成）：**
```bash
# 1枚目のプレビュー
docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --image png coconala-presentation.md --allow-local-files

# 全スライドのプレビュー
docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --images png coconala-presentation.md --allow-local-files

# プレビュー後のクリーンアップ
rm coconala-presentation*.png
```

### 2. ローカルMarp CLIを使用

**インストール：**
```bash
# Node.js環境が必要
npm install -g @marp-team/marp-cli
```

**使用：**
```bash
# PDF生成
marp --theme coconala-theme/coconala-pop.css --pdf --allow-local-files coconala-presentation.md

# プレビュー
marp --theme coconala-theme/coconala-pop.css --image png --allow-local-files coconala-presentation.md
```

## 📝 テンプレートの使用方法

### 基本的な手順

1. **テンプレートをコピー**
   ```bash
   cp coconala-presentation.md my-presentation.md
   ```

2. **内容を編集**
   - タイトル、発表者名、日付を変更
   - 章タイトルを実際の内容に変更
   - プレースホルダーコンテンツを実際の内容に置換

3. **PDF生成**
   ```bash
   docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --pdf my-presentation.md --allow-local-files
   ```

### スライドタイプの使い方

#### タイトルスライド
```markdown
<!-- _class: title-slide -->
<!-- _backgroundImage: url('coconala-theme/assets/images/title_bg.svg') -->

# メインタイトル<br />サブタイトル

<div class="subtitle">
イベント名・発表日 / YYYY-MM-DD<br/>
発表者名
</div>
```

#### アジェンダスライド
```markdown
<!-- _class: agenda -->
<!-- _backgroundImage: url('coconala-theme/assets/images/agenda_bg.svg') -->

# アジェンダ

- **第1章のタイトル**
- **第2章のタイトル**
- **第3章のタイトル**
...
```

#### 章構成（2ページセット）
```markdown
<!-- 章の導入ページ -->
<!-- _class: chapter-intro chapter-intro-01 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_1_bg.svg') -->

# 第1章のタイトル

---

<!-- 章のコンテンツページ -->
<!-- _class: chapter-page chapter-page-01 -->

# 第1章のタイトル

<div class="chapter-message">
  この章の要点やキーメッセージ
</div>

<div class="chapter-content equal">
  <div class="content-left">
    <h3>🎯 左側コンテンツ</h3>
    <ul>
      <li>ポイント1</li>
      <li>ポイント2</li>
    </ul>
  </div>
  <div class="content-right">
    <h3>✨ 右側コンテンツ</h3>
    <p><strong>重要なメッセージ</strong></p>
    <p>詳細説明</p>
  </div>
</div>
```

#### クロージングページ
```markdown
<!-- _class: closing-page -->
<!-- _backgroundImage: url('coconala-theme/assets/images/closing_page_bg.svg') -->

# ご清聴ありがとうございました

## お気軽にお声がけください

<div class="subtitle">
メッセージ
</div>

<div class="contact-info">
  <strong>ウェブサイト：</strong> <a href="https://example.com">https://example.com</a><br/>
  <strong>メール：</strong> <a href="mailto:contact@example.com">contact@example.com</a><br/>
  <strong>SNS：</strong> <a href="https://x.com/username">@username</a>
</div>
```

## 🎨 レイアウトパターン

### chapter-contentのレイアウト選択

- **equal**: 5:5の左右分割
  ```html
  <div class="chapter-content equal">
    <div class="content-left">...</div>
    <div class="content-right">...</div>
  </div>
  ```

- **single**: 全幅使用
  ```html
  <div class="chapter-content single">
    <div class="content-single">...</div>
  </div>
  ```

- **ratio-7-3**: 7:3の左右分割
  ```html
  <div class="chapter-content ratio-7-3">
    <div class="content-left">...</div>
    <div class="content-right">...</div>
  </div>
  ```

## 🔧 カスタマイズ

### 章の色とブランディング

各章は以下の色で自動設定されます：

- **Chapter 1**: ブルー (`#0085ff`)
- **Chapter 2**: グリーン (`#00c48f`)
- **Chapter 3**: イエロー (`#ffcc00`)
- **Chapter 4**: オレンジ (`#ff9b35`)
- **Chapter 5**: ピンク (`#ff4a8c`)
- **Chapter 6**: パープル (`#9164ff`)

色を変更する場合は `coconala-theme/coconala-pop.css` の該当部分を編集してください。

### 新しい章の追加

現在は6章まで対応していますが、7章目以降を追加する場合：

1. CSS に新しい章のスタイルを追加
2. 対応する三角形SVGアイコンを作成
3. 章背景画像を作成

## 🐛 トラブルシューティング

### よくある問題

**1. 画像が表示されない**
```bash
# --allow-local-files オプションを確認
docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --pdf coconala-presentation.md --allow-local-files
```

**2. 三角形アイコンが表示されない**
- `coconala-theme/assets/images/triangle-with-X.svg` ファイルの存在を確認
- CSS内の相対パスが正しいか確認

**3. フォントが読み込まれない**
- `coconala-theme/assets/fonts/M_PLUS_1p/` フォルダとフォントファイルの存在を確認

**4. レイアウトが崩れる**
- コンテンツが長すぎる場合は文章を短縮
- 適切な `chapter-content` レイアウトクラスを使用

### デバッグ手順

1. **HTMLプレビューで確認**
   ```bash
   docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --html coconala-presentation.md --allow-local-files
   ```

2. **1枚ずつ確認**
   ```bash
   docker run --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli --theme coconala-theme/coconala-pop.css --image png coconala-presentation.md --allow-local-files
   ```

3. **エラーログを確認**
   - Dockerコマンドの出力にエラーメッセージがないか確認

## 🔗 参考リンク

- [Marp 公式サイト](https://marp.app/)
- [Marp CLI ドキュメント](https://github.com/marp-team/marp-cli)
- [Marp CLI Docker Hub](https://hub.docker.com/r/marpteam/marp-cli/)
- [Markdown記法ガイド](https://www.markdownguide.org/)

## 📄 ライセンス

このテンプレートはMITライセンスの下で提供されています。

---

**Happy Presenting! 🎤** 