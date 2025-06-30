---
marp: true
theme: corporate-blue-green
paginate: true
header: "Cursor勉強会 - AI駆動開発"
footer: "2025.07.05 | Women's Base"
---

<!-- 
テーマの使い方：
1. このファイルと同じディレクトリに marp-corporate-theme.css を配置
2. VS Codeの設定またはMarp CLIでテーマファイルを指定
3. themeに "corporate-blue-green" を指定
-->

<!-- _class: title -->

# Cursor勉強会
## AIペアプログラミングの実践

2025年7月5日
Women's Base エンジニアコミュニティ

---

# アジェンダ

1. **イントロダクション**（5分）
2. **Cursorの基本概要**（10分）
3. **よく使う主要機能**（15分）
4. **Cursor 1.0の新機能**（10分）
5. **他のAI IDEとの比較**（5分）
6. **実務での活用Tips**（5分）

---

<!-- _class: section -->

# 1. イントロダクション

---

# Cursorとは？

<div class="point-box">
<h4>🎯 ポイント</h4>
<p><strong>AI駆動型の統合開発環境（IDE）</strong></p>
</div>

- Visual Studio Codeをフォークして開発
- AIが深く統合された開発環境
- コードベース全体を理解し、自然言語で対話可能

---

# なぜCursorが注目されているのか

## 3つの革新

1. **開発効率の劇的な向上**
   - コード生成速度が10倍以上に
   - デバッグ時間を50%削減

2. **「思考の速度でコーディング」**
   - アイデアから実装までのギャップを最小化
   - 自然言語で指示するだけ

3. **グラントワークからの解放**
   - 繰り返し作業の自動化
   - より創造的な作業に集中可能

---

<!-- _class: two-column -->

# 主要機能の例

<div>

## Tab補完
```python
def process_data(data):
    threshold = 0.5
    # AIが自動的に補完
```

## Ctrl+K（インライン編集）
```javascript
// "最適化して"と指示
const sum = numbers.reduce(
  (a, b) => a + b, 0
);
```

</div>

<div>

## Agent機能
- 複雑なタスクを自律実行
- 複数ファイルの一括変更
- テスト自動生成

## チャット機能
- コードに関する質問
- バグの特定と修正
- @シンボルでコンテキスト管理

</div>

---

<!-- _class: emphasis -->

# Cursor 1.0の新機能

<ul class="icon-list">
<li><strong>Agent機能</strong> - 自律的なコーディングパートナー</li>
<li><strong>BugBot</strong> - GitHub PRの自動レビュー</li>
<li><strong>バックグラウンドエージェント</strong> - 並行作業で生産性向上</li>
<li><strong>メモリー機能</strong> - 過去の会話を記憶</li>
</ul>

---

# 他のAI IDEとの比較

| 機能 | Cursor | GitHub Copilot | Claude Code |
|------|--------|----------------|-------------|
| コードベース理解 | ◎ | △ | ○ |
| 自律的タスク実行 | ◎ | × | △ |
| 複数ファイル編集 | ◎ | △ | ○ |
| IDE統合の深さ | ◎ | ○ | △ |

<div class="progress" style="--progress: 70%"></div>

---

<!-- _class: code-sample -->

# 実践例：ダークモード実装

```typescript
// Agentへの指示：「アプリにダークモードを追加して」

// 1. テーマコンテキストの作成
export const ThemeContext = createContext({
  theme: 'light',
  toggleTheme: () => {}
});

// 2. CSS変数の定義
:root {
  --bg-color: #ffffff;
  --text-color: #000000;
}
[data-theme="dark"] {
  --bg-color: #1a1a1a;
  --text-color: #ffffff;
}
```

---

# 実務での活用Tips

<div class="caution-box">
<h4>⚠️ 注意点</h4>
<ul>
<li>AIの提案を盲信しない</li>
<li>大規模ファイルでのパフォーマンス低下</li>
<li>レートリミットに注意</li>
</ul>
</div>

## ベストプラクティス

1. **明確なプロンプト**を心がける
2. **段階的な実装**アプローチ
3. **定期的なコードレビュー**

---

<!-- _class: summary -->

# まとめ

- Cursorは「思考の速度」でコーディングを可能に
- AIペアプログラマーとして開発効率を向上
- 適切な使い方で生産性を最大化

## 次のステップ

- ハンズオンでVibe Codingを体験
- 実際のプロジェクトで活用
- チームでの導入を検討

---

<!-- _class: title -->

# ありがとうございました

## 質問・ディスカッション

ハンズオンで実際に体験してみましょう！