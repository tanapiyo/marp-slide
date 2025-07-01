# Cursor勉強会スライド構成案
## 女性エンジニアコミュニティ向け（50分・50ページ）

---

## 目次構成

### 第1章：イントロダクション（5ページ）
1. タイトルスライド
2. 本日のゴール - AIペアプログラミングで開発効率を変える
3. アジェンダ
4. Cursorとは？ - 30秒で理解する
5. なぜ今Cursorなのか - AI開発の現在地

### 第2章：Cursorの基本概要（5ページ）
6. Cursor IDE の位置づけ
7. 導入事例 - 開発効率が変わった企業・個人の声
8. Cursorができること - 一覧
9. 料金プラン比較
10. セットアップの流れ（既存VSCodeからの移行含む）

### 第3章：基本機能の理解（15ページ）
11. 機能全体マップ
12. Tab補完 - 最も使う基本機能
13. Tab補完の実例（Python/JavaScript）
14. Ctrl+K（Cmd+K）- インラインコード生成
15. Ctrl+Kの実例 - 関数の実装
16. Ctrl+Kの実例 - リファクタリング
17. Chat（Ctrl+L）- AIとの対話
18. Chatの実例 - エラー解決
19. @記号の活用 - コンテキスト指定
20. @Filesの実例 - 複数ファイルを考慮した修正
21. @Codebaseの実例 - プロジェクト全体の理解
22. @Docsの実例 - ドキュメント参照
23. @Webの実例 - 最新情報の取得
24. Composerモード - マルチファイル編集
25. Composerの実例 - 新機能の実装
26. Agent Mode - 背景での自動処理
27. Agent Modeの実例 - バックグラウンド実行

### 第4章：Rulesによる開発体験のカスタマイズ（10ページ）
28. Rulesとは - AIの振る舞いをコントロール
29. Rules階層構造 - User/Project/Custom
30. User Rulesの設定例 - 個人の好みを反映
31. Project Rulesの実例 - チーム開発での統一
32. Rules実例1：コーディング規約の徹底
33. Rules実例2：セキュリティ考慮の自動化
34. Rules実例3：テストコード生成の標準化
35. Rules実例4：ドキュメント生成の自動化
36. Awesome Cursor Rulesの活用
37. Rulesのベストプラクティス

### 第5章：Cursor 1.0の新機能（5ページ）
38. Cursor 1.0アップデート概要
39. BugBot - GitHub PR自動レビュー
40. Memories - プロジェクト情報の記憶
41. Multi-Cursor (MCP) - 初期サポート
42. その他の新機能と改善点

### 第6章：実践的な活用（5ページ）
43. Privacy Modeの使い方 - 機密情報の保護
44. モデルの選び方ガイド
45. モデル比較表（GPT-4o、Claude 3.5、Gemini 2.0 Pro）
46. Cursorの内部構成 - なぜ速いのか
47. トラブルシューティングTips

### 第7章：他のAI開発ツールとの比較（4ページ）
48. AI開発ツール全体マップ
49. 機能比較表（Copilot、Claude Code、Cline、Devin）
50. 自走度と人の介在度の比較
51. 適材適所 - ツールの使い分け指針

### 第8章：まとめと次のステップ（1ページ）
52. 本日のまとめ - Cursorで変わる開発体験

---

## 詳細内容

### 第1章：イントロダクション

#### スライド1：タイトルスライド
# CursorでAI時代の開発を体験する
## 女性エンジニアコミュニティ勉強会
### 2025年1月

---

#### スライド2：本日のゴール
# AIペアプログラミングで開発効率を変える

- **Before**: コード書く → エラー調べる → 修正 → テスト書く
- **After**: アイデア伝える → AI生成 → レビュー → 完成

### 本日学ぶこと
- Cursorの全機能を理解する
- 自分の開発スタイルに合わせた使い方を見つける
- 明日から使える実践的なTipsを習得する

---

#### スライド3：アジェンダ
# 本日の流れ（50分）

1. **基本概要**（5分）- Cursorって何？
2. **基本機能**（15分）- 毎日使う機能
3. **Rules詳解**（10分）- カスタマイズの極意
4. **新機能**（5分）- Cursor 1.0の革新
5. **実践活用**（10分）- プロ級の使い方
6. **他ツール比較**（5分）- 使い分けガイド

---

#### スライド4：Cursorとは？
# 30秒で理解するCursor

## AIネイティブなコードエディタ
- VSCodeをベースに、AI機能を統合
- コーディングの**すべての場面**でAIがサポート
- **考える時間を増やし、作業時間を減らす**

### キーワード
```
補完 → 生成 → 対話 → 自動化
```

---

#### スライド5：なぜ今Cursorなのか
# AI開発の現在地

## 開発者の声（2024年調査）
- 「コード生成で開発速度が**2-3倍**に」
- 「デバッグ時間が**60%削減**」
- 「新しい言語の学習が**格段に速く**」

### Cursorのシェア
- GitHub Stars: **25,000+** (2024年12月)
- 月間アクティブユーザー: **100万人突破**
- 大手テック企業での採用事例増加

*出典: Cursor公式発表、GitHub統計*

---

### 第2章：Cursorの基本概要

#### スライド6：Cursor IDEの位置づけ
# エディタ × AI の進化

```
テキストエディタ → IDE → AI搭載IDE → AIネイティブIDE
   (Vim/Emacs)   (VSCode)  (Copilot)      (Cursor)
```

### Cursorの特徴
- **統合度**: AIが全機能に深く統合
- **コンテキスト理解**: プロジェクト全体を把握
- **対話的**: チャットで要求を伝えられる

---

#### スライド7：導入事例
# 開発効率が変わった声

## 事例1：スタートアップA社
> 「新機能の実装が**3日→1日**に短縮」

## 事例2：フリーランスBさん
> 「苦手なフロントエンドも**自信を持って**書ける」

## 事例3：大手C社
> 「ジュニアエンジニアの**成長速度が2倍**に」

*※実際のユーザーフィードバックより*

---

#### スライド8：Cursorができること
# 機能一覧

| カテゴリ | 機能 | 効果 |
|---------|------|------|
| **補完** | Tab補完 | コード記述を高速化 |
| **生成** | Ctrl+K、Composer | 新規実装を効率化 |
| **対話** | Chat、@記号 | 問題解決を迅速化 |
| **自動化** | Agent Mode | 作業を自動化 |
| **カスタマイズ** | Rules | 好みに最適化 |

---

#### スライド9：料金プラン比較
# 投資対効果を考える

| プラン | 月額 | 特徴 | おすすめ |
|--------|------|------|----------|
| **Free** | $0 | 基本機能、制限あり | お試し |
| **Pro** | $20 | 無制限、高速モデル | 個人開発 |
| **Business** | $40 | チーム機能、管理 | チーム |

### ROI計算例
時給5,000円 × 月20時間削減 = **月10万円の価値**

---

#### スライド10：セットアップの流れ
# 5分で始められる

## 新規インストール
1. cursor.com からダウンロード
2. インストール実行
3. アカウント作成/ログイン

## VSCodeからの移行
1. 設定の引き継ぎ: **自動**
2. 拡張機能: **そのまま使える**
3. キーバインド: **完全互換**

💡 **Tip**: まずFreeプランで試してみましょう

---

### 第3章：基本機能の理解

#### スライド11：機能全体マップ
# Cursorの機能体系

```mermaid
graph TD
    A[Cursor機能] --> B[補完系]
    A --> C[生成系]
    A --> D[対話系]
    A --> E[自動化系]
    
    B --> B1[Tab補完]
    C --> C1[Ctrl+K]
    C --> C2[Composer]
    D --> D1[Chat]
    D --> D2[@記号]
    E --> E1[Agent Mode]
```

---

#### スライド12：Tab補完
# 最も使う基本機能

## 特徴
- **予測的**: 次に書くコードを先読み
- **文脈理解**: 周辺コードから適切な提案
- **多言語対応**: あらゆる言語で動作

### 使い方
1. コードを書き始める
2. グレーの提案が表示
3. `Tab`キーで採用

---

#### スライド13：Tab補完の実例
# 実際の動作例

## Python例
```python
def calculate_total(items):
    # ここでTabを押すと...
    return sum(item.price * item.quantity for item in items)
```

## JavaScript例
```javascript
const users = await fetchUsers();
// ここでTabを押すと...
const activeUsers = users.filter(user => user.isActive);
```

💡 **Tip**: 変数名を分かりやすくすると精度UP

---

#### スライド14：Ctrl+K（Cmd+K）
# インラインコード生成

## 何ができる？
- 選択範囲の**書き換え**
- 新規コードの**生成**
- 既存コードの**リファクタリング**

### 基本操作
1. コード選択（または空行）
2. `Ctrl+K`（Mac: `Cmd+K`）
3. 指示を入力
4. Enter

---

#### スライド15：Ctrl+Kの実例 - 関数実装
# ゼロから関数を生成

## 指示例
```
Ctrl+K: ユーザーの年齢から世代を判定する関数を作成
```

## 生成結果
```python
def get_generation(age):
    """年齢から世代を判定する"""
    if age < 20:
        return "Z世代"
    elif age < 40:
        return "ミレニアル世代"
    elif age < 55:
        return "X世代"
    else:
        return "ベビーブーマー世代"
```

---

#### スライド16：Ctrl+Kの実例 - リファクタリング
# 既存コードの改善

## Before（選択してCtrl+K）
```javascript
// 指示: より読みやすくリファクタリング
if (user.age >= 18) {
    if (user.hasLicense) {
        if (car.isAvailable) {
            return true;
        }
    }
}
return false;
```

## After
```javascript
const isAdult = user.age >= 18;
const canDrive = user.hasLicense;
const carAvailable = car.isAvailable;

return isAdult && canDrive && carAvailable;
```

---

#### スライド17：Chat（Ctrl+L）
# AIとの対話

## 特徴
- **会話形式**: 自然な言葉で質問
- **コンテキスト保持**: 会話の流れを理解
- **コード提案**: 実装案を提示

### よくある使い方
- エラーの解決方法を聞く
- アーキテクチャの相談
- ベストプラクティスの確認

---

#### スライド18：Chatの実例 - エラー解決
# エラーメッセージを貼るだけ

## 質問例
```
このエラーの解決方法を教えてください：
TypeError: Cannot read property 'map' of undefined
```

## AIの回答
```markdown
このエラーは配列がundefinedの時にmapを呼んでいます。

解決方法：
1. デフォルト値を設定
   const items = data?.items || [];
   
2. 条件付きレンダリング
   {items && items.map(...)}
   
3. オプショナルチェーン
   {items?.map(...)}
```

---

#### スライド19：@記号の活用
# コンテキストを指定

## @の種類
- `@ファイル名`: 特定ファイルを参照
- `@Folders`: フォルダを参照
- `@Code`: コードシンボルを参照
- `@Codebase`: プロジェクト全体
- `@Docs`: ドキュメント検索
- `@Web`: Web検索

### 使い方
Chat内で`@`を入力して選択

---

#### スライド20：@Filesの実例
# 複数ファイルを考慮

## シナリオ
```
@user.py @database.py 
これらのファイルを参照して、ユーザー登録機能を実装してください
```

## AIの対応
- 両ファイルの構造を理解
- 整合性のある実装を提案
- インポート文も自動生成

---

#### スライド21：@Codebaseの実例
# プロジェクト全体の理解

## 質問例
```
@Codebase
このプロジェクトのアーキテクチャを説明してください
```

## AIの分析結果
```
プロジェクト構造：
- MVCパターンを採用
- models/: データモデル定義
- views/: UIコンポーネント
- controllers/: ビジネスロジック

主要な依存関係：
- Django 4.0
- PostgreSQL
- Redis（キャッシュ）
```

---

#### スライド22：@Docsの実例
# ドキュメント参照

## 使用例
```
@Docs React hooks
useEffectの正しい使い方を教えてください
```

## メリット
- 公式ドキュメントに基づく正確な情報
- 最新のベストプラクティス
- 実装例付きの説明

---

#### スライド23：@Webの実例
# 最新情報の取得

## 活用シーン
```
@Web Next.js 14 新機能
App Routerの使い方を教えてください
```

## 得られる情報
- 最新バージョンの機能
- 実装サンプル
- 注意点や既知の問題

---

#### スライド24：Composerモード
# マルチファイル編集

## 特徴
- **複数ファイル同時編集**
- **一貫性のある変更**
- **大規模リファクタリング対応**

### アクセス方法
`Ctrl+I`（Mac: `Cmd+I`）

---

#### スライド25：Composerの実例
# 新機能の実装

## 指示例
```
ユーザープロフィール編集機能を追加してください：
- APIエンドポイント作成
- フロントエンドフォーム作成
- バリデーション追加
- テストコード作成
```

## 生成されるファイル
- `api/users/profile.py`
- `components/ProfileForm.jsx`
- `validators/userProfile.js`
- `tests/profile.test.js`

---

#### スライド26：Agent Mode
# 背景での自動処理

## 特徴
- **非同期実行**: 他の作業をしながらAIが作業
- **複数タスク**: 調査、修正、ドキュメント作成を並行
- **プロジェクト理解**: 全体を把握した上で作業

### 使用シーン
- 大量のリファクタリング
- レガシーコードの調査
- テスト網羅性の向上

---

#### スライド27：Agent Modeの実例
# バックグラウンド実行

## 指示例
```
Agent: このプロジェクトのすべてのTypeScriptエラーを調査し、
修正計画を立ててください。私は他の機能開発を続けます。
```

## Agentの作業内容
```
🔍 実行中...
- TypeScriptエラー検出: 24件
- 影響範囲の分析: 8ファイル
- 修正優先度の設定: 完了
- 修正案の作成: 進行中
```

### 通知タイミング
作業完了時に結果レポートを表示

---

### 第4章：Rulesによる開発体験のカスタマイズ

#### スライド28：Rulesとは
# AIの振る舞いをコントロール

## Rulesの目的
- コーディング規約の**自動適用**
- チーム開発の**一貫性確保**
- 個人の好みの**反映**

### 設定できること
- コードスタイル
- 命名規則
- コメントの書き方
- エラーハンドリング方針

---

#### スライド29：Rules階層構造
# 3つのレベル

```
┌─────────────────┐
│  Custom Rules   │ ← タスク特有
├─────────────────┤
│ Project Rules   │ ← プロジェクト共通
├─────────────────┤
│  User Rules     │ ← 個人設定
└─────────────────┘
```

### 優先順位
Custom > Project > User

---

#### スライド30：User Rulesの設定例
# 個人の好みを反映

## 設定ファイル: `~/.cursor/rules`
```yaml
# 私のコーディングスタイル
style:
  - 日本語のコメントを使用
  - 変数名は分かりやすく
  - 早期リターンを優先

language_specific:
  python:
    - Type hintsを必ず使用
    - docstringはGoogle形式
  javascript:
    - constを優先、letは必要時のみ
    - アロー関数を使用
```

---

#### スライド31：Project Rulesの実例
# チーム開発での統一

## `.cursor/rules` （プロジェクトルート）
```yaml
# チーム共通ルール
team_conventions:
  - コミットメッセージは英語
  - PRには必ずテストを含める
  - エラーは詳細にログ出力

architecture:
  - Clean Architectureに従う
  - DIコンテナを使用
  - Repository patternで実装

security:
  - 入力値は必ず検証
  - SQLインジェクション対策必須
  - 機密情報はenvファイルへ
```

---

#### スライド32：Rules実例1
# コーディング規約の徹底

## Rule設定
```yaml
coding_standards:
  - 関数は単一責任の原則に従う
  - 関数は20行以内
  - ネストは3段階まで
```

## 適用結果
```python
# AIが生成するコード
def process_order(order_data):
    """注文を処理する（20行以内）"""
    validated_data = _validate_order(order_data)
    payment_result = _process_payment(validated_data)
    shipping_info = _arrange_shipping(validated_data)
    
    return {
        'order_id': validated_data['id'],
        'payment': payment_result,
        'shipping': shipping_info
    }

# 別関数に分割される
def _validate_order(data):
    # バリデーションロジック
    pass
```

---

#### スライド33：Rules実例2
# セキュリティ考慮の自動化

## Rule設定
```yaml
security_rules:
  - SQLクエリは必ずプレースホルダ使用
  - ユーザー入力は必ずサニタイズ
  - パスワードは必ずハッシュ化
```

## 生成されるコード
```python
# ユーザー登録処理
def register_user(email, password):
    # 入力値のサニタイズ（自動追加）
    email = sanitize_email(email)
    
    # パスワードのハッシュ化（自動追加）
    hashed_password = bcrypt.hashpw(
        password.encode('utf-8'), 
        bcrypt.gensalt()
    )
    
    # プレースホルダを使用（自動適用）
    query = "INSERT INTO users (email, password) VALUES (?, ?)"
    db.execute(query, (email, hashed_password))
```

---

#### スライド34：Rules実例3
# テストコード生成の標準化

## Rule設定
```yaml
testing_rules:
  - すべての関数にユニットテスト作成
  - テストはAAA形式（Arrange-Act-Assert）
  - エッジケースを必ず含める
  - モックは最小限に
```

## 生成されるテスト
```python
def test_calculate_discount():
    # Arrange
    original_price = 1000
    discount_rate = 0.2
    
    # Act
    result = calculate_discount(original_price, discount_rate)
    
    # Assert
    assert result == 800
    
def test_calculate_discount_edge_cases():
    # ゼロ割引
    assert calculate_discount(1000, 0) == 1000
    # 100%割引
    assert calculate_discount(1000, 1.0) == 0
    # 負の価格（エラー）
    with pytest.raises(ValueError):
        calculate_discount(-100, 0.2)
```

---

#### スライド35：Rules実例4
# ドキュメント生成の自動化

## Rule設定
```yaml
documentation_rules:
  - すべての公開関数にdocstring
  - 引数と戻り値の型と説明
  - 使用例を含める
  - エラーケースも記載
```

## 生成されるドキュメント
```python
def fetch_user_data(user_id: int, include_details: bool = False) -> dict:
    """
    ユーザーデータを取得する
    
    Args:
        user_id (int): ユーザーID
        include_details (bool): 詳細情報を含めるか（デフォルト: False）
    
    Returns:
        dict: ユーザー情報を含む辞書
    
    Example:
        >>> user = fetch_user_data(123)
        >>> print(user['name'])
        'John Doe'
        
        >>> detailed = fetch_user_data(123, include_details=True)
        >>> print(detailed['created_at'])
        '2024-01-01'
    
    Raises:
        UserNotFoundError: 指定されたユーザーが存在しない場合
        DatabaseError: データベース接続エラーが発生した場合
    """
```

---

#### スライド36：Awesome Cursor Rules
# コミュニティの知恵を活用

## GitHubリポジトリ
https://github.com/PatrickJS/awesome-cursorrules

### 人気のRules例
- **clean-code**: クリーンコードの原則
- **react-best-practices**: React開発のベストプラクティス
- **python-zen**: Pythonの禅に従った開発
- **security-first**: セキュリティ重視の開発

### 使い方
1. リポジトリから選ぶ
2. `.cursor/rules`にコピー
3. 必要に応じてカスタマイズ

---

#### スライド37：Rulesのベストプラクティス
# 効果的なRules設定のコツ

## DO ✅
- **具体的に書く**: 「良いコード」より「関数は20行以内」
- **段階的に導入**: 一度に多くのルールは混乱の元
- **チームで議論**: Project Rulesは合意形成が重要
- **定期的に見直し**: プロジェクトの成長に合わせて更新

## DON'T ❌
- **抽象的すぎる指示**: AIが解釈に迷う
- **矛盾するルール**: 優先順位を明確に
- **過度な制約**: 創造性を阻害しない程度に

### 💡 Tip
まずは3-5個の重要なルールから始めましょう

---

### 第5章：Cursor 1.0の新機能

#### スライド38：Cursor 1.0アップデート概要
# AIとの共同開発を進化させる

## 主要な新機能
1. **BugBot**: GitHub PR自動レビュー
2. **Memories**: プロジェクト情報の記憶
3. **Multi-Cursor (MCP)**: 初期サポート
4. **Background Agent**: 非同期タスク実行

### 設計思想
「**AIが開発者の意図を理解し、協働する**」

*出典: Cursor 1.0 リリース記事*

---

#### スライド39：BugBot
# GitHub PR自動レビュー

## 機能概要
- **自動PR分析**: コード変更の影響を評価
- **バグ検出**: 潜在的な問題を発見
- **改善提案**: より良い実装方法を提案

### 動作例
```markdown
🤖 BugBot Review

❌ 潜在的な問題:
- L23: null チェックが不十分
- L45: メモリリークの可能性

✅ 改善提案:
- Optional chaining の使用
- useEffect のクリーンアップ追加
```

---

#### スライド40：Memories
# プロジェクト情報の記憶

## 機能概要
- **プロジェクト理解**: アーキテクチャやルールを記憶
- **コンテキスト保持**: 過去の会話や決定事項を覚える
- **個人化**: 開発者の好みやパターンを学習

### 活用例
```
💭 Memories

- このプロジェクトはClean Architectureを採用
- テストはJestとReact Testing Library
- APIはGraphQLを使用
- 前回の相談: パフォーマンス最適化について
```

---

#### スライド41：Multi-Cursor (MCP)
# 複数箇所同時編集の進化

## 新機能
- **AI支援マルチカーソル**: 類似パターンを自動検出
- **コンテキスト理解**: 各箇所の文脈を考慮した編集
- **一括変換**: 命名規則変更なども一括対応

### 使用例
- 変数名の一括変更（スコープを考慮）
- 類似関数の同時リファクタリング
- テストケースの一括生成

---

#### スライド42：その他の新機能
# 開発体験の向上

## Jupyter Notebook統合
- データ分析コードの自動生成
- グラフ作成支援
- 分析結果の解釈提案

## リッチなChat応答
- **Mermaid.js図表**: フローチャートやER図を自動生成
- **コードハイライト**: より見やすい表示
- **段階的説明**: 複雑な概念を分解して説明

## 設定・ダッシュボード改善
- より直感的なUI
- 使用統計の可視化
- チーム設定の簡素化

---

### 第6章：実践的な活用

#### スライド43：Privacy Mode
# 機密情報の保護

## Privacy Modeとは
- コードがクラウドに**送信されない**
- ローカルモデルで動作
- 企業の機密情報を守る

### 有効化方法
1. 設定 → Privacy
2. "Privacy Mode"をON
3. 必要に応じてファイル単位で設定

### 💡 使用シーン
- 顧客データを扱うコード
- 社内システムの開発
- 特許申請前のアルゴリズム

---

#### スライド44：モデルの選び方ガイド
# 用途別おすすめモデル

## 基本方針
```
速度重視 → GPT-4o
品質重視 → Claude 3.5 Sonnet
バランス → Gemini 2.0 Pro
```

### 詳細な使い分け
- **単純な補完**: GPT-4o（高速）
- **複雑なロジック**: Claude 3.5（推論力）
- **多言語対応**: Gemini 2.0（幅広い知識）
- **長文生成**: Claude 3.5（一貫性）

---

#### スライド45：モデル比較表
# 性能・特徴比較

| モデル | 速度 | 品質 | コスト | 得意分野 |
|--------|------|------|--------|----------|
| GPT-4o | ⚡⚡⚡ | ⭐⭐⭐ | $ | 汎用・高速処理 |
| Claude 3.5 Sonnet | ⚡⚡ | ⭐⭐⭐⭐⭐ | $$ | 複雑な推論・長文 |
| Gemini 2.0 Pro | ⚡⚡⚡ | ⭐⭐⭐⭐ | $ | マルチモーダル |
| GPT-o3 | ⚡ | ⭐⭐⭐⭐⭐ | $$$ | 最高品質（制限あり） |

### 切り替え方法
チャット画面上部のモデル選択ボタンから変更

---

#### スライド46：Cursorの内部構成
# なぜ速いのか

## 技術的な工夫
```
ユーザー入力
    ↓
コンテキスト構築（ローカル）
    ↓
最適化されたプロンプト
    ↓
並列API呼び出し
    ↓
ストリーミング応答
```

### キーポイント
- **ローカルインデックス**: コードベースを事前解析
- **差分同期**: 変更部分のみ送信
- **キャッシュ活用**: 類似リクエストを高速化

---

#### スライド47：トラブルシューティング
# よくある問題と解決法

## 症状別対処法

### 補完が遅い
→ モデルをGPT-4oに変更
→ キャッシュクリア（設定から）

### 提案が的外れ
→ Rulesを見直す
→ より具体的な変数名に

### エラーが発生
→ Cursor再起動
→ 拡張機能の競合確認

### 料金が高い
→ 使用モデルの見直し
→ Privacy Modeの活用

---

### 第7章：他のAI開発ツールとの比較

#### スライド48：AI開発ツール全体マップ
# 各ツールの立ち位置

```
        高自律性
           ↑
    Devin  |  Agent Mode
           |
    Cline  |  Cursor
           |  Claude Code
  Copilot  |
           |
        低自律性
    シンプル ← → 高機能
```

---

#### スライド49：機能比較表
# 主要AI開発ツール比較

| 機能 | Cursor | Copilot | Claude Code | Cline | Devin |
|------|--------|---------|-------------|-------|-------|
| IDE統合 | ◎ | ◎ | ○ | △ | × |
| 対話機能 | ◎ | △ | ◎ | ○ | ◎ |
| 自律動作 | ○ | × | △ | ○ | ◎ |
| マルチファイル | ◎ | △ | ○ | ◎ | ◎ |
| カスタマイズ | ◎ | △ | ○ | ○ | △ |
| 価格 | $$ | $ | $$ | Free | $$$ |

◎:優秀 ○:対応 △:限定的 ×:非対応

---

#### スライド50：自走度と人の介在度
# どこまでAIに任せるか

## ツール別の特徴
```
人の介在度: 高 ← → 低
Copilot → Cursor → Claude Code → Cline → Devin

タスクサイズ: 小 ← → 大
行単位 → 関数単位 → ファイル単位 → 機能単位 → プロジェクト
```

### 使い分けの指針
- **細かい制御**: Copilot
- **バランス型**: Cursor
- **対話重視**: Claude Code
- **自動化重視**: Cline/Devin

---

#### スライド51：適材適所
# ツールの使い分け指針

## シーン別おすすめ

### 日常のコーディング
→ **Cursor**: 高速補完＋必要時に対話

### ペアプログラミング
→ **Claude Code**: 対話しながら開発

### 定型作業の自動化
→ **Cline**: スクリプト的な処理

### 新規開発の丸投げ
→ **Devin**: 要件から実装まで

### 既存IDEを変えたくない
→ **Copilot**: プラグインとして導入

---

### 第8章：まとめ

#### スライド52：本日のまとめ
# Cursorで変わる開発体験

## 学んだこと
✅ 基本機能（Tab、Ctrl+K、Chat、@記号）
✅ Rulesによるカスタマイズ
✅ Cursor 1.0の新機能
✅ 実践的な活用方法
✅ 他ツールとの使い分け

## 次のアクション
1. **今日**: Cursorをインストール
2. **今週**: 基本機能を使ってみる
3. **来週**: Rulesを設定してみる
4. **来月**: チームに展開を検討

### 🚀 Let's start AI-powered coding!

---

# 補足資料

## 参考リンク
- Cursor公式: https://cursor.com
- Cursor Docs: https://docs.cursor.com
- Awesome Cursor Rules: https://github.com/PatrickJS/awesome-cursorrules
- コミュニティフォーラム: https://forum.cursor.com

## 学習リソース
- YouTube: Cursor公式チャンネル
- Zenn: Cursor関連記事
- Qiita: 実践Tips集

## お問い合わせ
ご質問は勉強会Slackチャンネルまで！