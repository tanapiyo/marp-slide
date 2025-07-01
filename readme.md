# cursor-lecture

## 概要
このリポジトリは、AIを活用してスライド構成（アウトライン）を自動生成し、Marpで高品質なスライドを作成する実験的プロジェクトです。

- AIによる業務用スライド構成案の自動生成
- Marpによるスライド化・カスタムテーマ適用の検証
- ビジネスプレゼンテーションのベストプラクティス集約

---

## Marpの使い方

### 1. Marp for VS Code 拡張のインストール
- VS Codeの拡張機能から「Marp for VS Code」をインストール

### 2. スライドMarkdownの作成
- `.md`ファイルの冒頭に以下を記載
  ```markdown
  ---
  marp: true
  theme: default  # またはカスタムテーマ名
  paginate: true
  ---
  ```
- 通常のMarkdown記法でスライドを記述
- `---`でスライド区切り

### 3. スライドのプレビュー方法
- VS CodeでスライドMarkdownファイルを開く
- 右上の「Marp: Open Preview」ボタン（または右クリックメニュー「Marp: Open Preview」）をクリック
- 別ウィンドウでスライド形式のプレビューが表示されます

### 4. PDF出力方法
- プレビュー画面右上の「Export」ボタンから「Export as PDF」を選択
  または
- コマンドパレット（Cmd+Shift+P）で「Marp: Export Slide Deck...」を実行し、PDF形式を選択
- 指定した場所にPDFが出力されます

---

## marp-sampleフォルダのカスタムテーマの使い方

### 1. テーマCSSの配置
- `marp-sample/marp-corporate-theme.css` を `marp-sample/` フォルダに配置

### 2. テーマ名の確認
- CSSファイル冒頭に `/* @theme corporate-blue-green */` の記載があることを確認

### 3. カスタムテーマの適用
- スライドMarkdown冒頭で `theme: corporate-blue-green` を指定
- 例：
  ```markdown
  ---
  marp: true
  theme: corporate-blue-green
  paginate: true
  ---
  ```

### 4. VS Codeでのカスタムテーマ設定
- `.vscode/settings.json` に以下を追加
  ```json
  {
    "marp.customTheme": ["marp-sample/marp-corporate-theme.css"]
  }
  ```
- これでMarp for VS Codeがカスタムテーマを認識します

---

## ディレクトリ構成例
```
cursor-lecture/
├── marp-sample/
│   ├── marp-corporate-theme.css
│   ├── marp-setup-guide.md
│   └── marp-theme-usage.md
├── slide-rules/
│   ├── marp-business-presentation-guide.md
│   └── marp-visual-guide.md
├── cursor-detailed_slides_v2.md
├── cursor_slide_outline.md
├── README.md
└── ...
```

---

## 参考
- [Marp公式ドキュメント](https://marp.app/)
- [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)

---

## ライセンス
本リポジトリの内容はMITライセンスで公開されています。
