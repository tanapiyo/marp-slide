# Marpテーマの使い方ガイド

## セットアップ方法

### 1. VS Code拡張機能のインストール
```bash
# VS Code Marketplaceから「Marp for VS Code」をインストール
```

### 2. VS Codeの設定

`settings.json`に以下を追加：

```json
{
  "markdown.marp.themes": [
    "./marp-corporate-theme.css"
  ]
}
```

### 3. Marp CLIでの使用

```bash
# インストール
npm install -g @marp-team/marp-cli

# PDFエクスポート
marp marp-theme-usage.md --pdf --theme ./marp-corporate-theme.css

# HTMLエクスポート
marp marp-theme-usage.md --html --theme ./marp-corporate-theme.css

# PPTXエクスポート
marp marp-theme-usage.md --pptx --theme ./marp-corporate-theme.css
```

## テーマクラスの使い方

### タイトルスライド
```markdown
<!-- _class: title -->
# メインタイトル
## サブタイトル
```

### セクション区切り
```markdown
<!-- _class: section -->
# セクションタイトル
```

### 強調スライド
```markdown
<!-- _class: emphasis -->
# 強調したい内容
```

### 2カラムレイアウト
```markdown
<!-- _class: two-column -->
# タイトル
<div>
左カラムの内容
</div>
<div>
右カラムの内容
</div>
```

### コードサンプル
```markdown
<!-- _class: code-sample -->
# コード例
```

### サマリー
```markdown
<!-- _class: summary -->
# まとめ
```

## カスタム要素の使い方

### ポイントボックス
```html
<div class="point-box">
<h4>🎯 ポイント</h4>
<p>重要な内容</p>
</div>
```

### 注意事項ボックス
```html
<div class="caution-box">
<h4>⚠️ 注意</h4>
<p>注意すべき内容</p>
</div>
```

### アイコン付きリスト
```html
<ul class="icon-list">
<li>項目1</li>
<li>項目2</li>
</ul>
```

### プログレスバー
```html
<div class="progress" style="--progress: 70%"></div>
```

## カラーパレット

- **濃い青**: `#227E93` - 見出し、強調
- **薄い青**: `#50B4CD` - アクセント、リンク
- **濃い緑**: `#212121` - テキスト、サブ見出し
- **薄い緑**: `#B2D855` - ハイライト、ボーダー
- **薄い青（追加）**: `#A0D2E0`, `#D0E9F2` - 背景
- **薄い緑（追加）**: `#D4E8A0`, `#E8F2D0` - 背景

## Tips

1. **フォント**: Noto Sans JPをメインに使用（日本語対応）
2. **コードフォント**: JetBrains Monoを推奨
3. **画像**: 自動的に角丸と影付きで表示
4. **アニメーション**: `.fade-in`クラスでフェードイン効果

## トラブルシューティング

### テーマが適用されない場合
1. CSSファイルのパスが正しいか確認
2. VS Codeを再起動
3. Markdownファイルのfrontmatterでtheme名を確認

### 文字が見切れる場合
- セクションのpaddingを調整
- フォントサイズを小さく設定

### PDFエクスポート時の問題
- `--allow-local-files`オプションを追加
- 日本語フォントがインストールされているか確認