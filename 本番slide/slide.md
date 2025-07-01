---
marp: true
theme: corporate-blue-green
paginate: true
header: "Cursor勉強会"
footer: "2025.07.05 | AI駆動開発勉強会 Women's Base"
---

## Cursor基礎講座

#### AI駆動開発勉強会 Women's Base
##### 2025年7月5日



---

## 本日のゴール

### Cursorを使える！と思ってもらう
#### 本日学ぶこと
- ✅ Cursorの**主要な機能機能**を理解する
- ✅ 自分の開発スタイルに合わせた**使い方を見つける**
- ✅ 明日から使える**Vibe Coding**を習得する

<!--
**説明者ノート：**
- 具体的な効率化のイメージを持ってもらう
- 参加者の現在の課題を聞いてもよい
-->
---

## アジェンダ

### 本日の流れ（50分）

| 時間 | 内容 |
|------|------|
| 5分 | 基本概要 - Cursorって何？ |
| 17分 | 基本機能 - 毎日使う機能 |
| 10分 | **Rules詳解** - カスタマイズの極意 |
| 5分 | 新機能 - Cursor 1.0の革新 |
| 8分 | 実践活用 - プロ級の使い方 |
| 4分 | 他ツール比較 - 使い分けガイド |
| 1分 | まとめ |

<!--
<!--
**説明者ノート：**
- 時間配分を意識しながら進行
- 質問は随時受け付ける旨を伝える
-->
---

## Cursorとは？

#### 🤖 AIネイティブなコードエディタ
- VSCodeをベースに、**AI機能を統合**
- コード生成・リファクタ・デバッグ・検索などを効率化できる
- 効果的なコード検索ができる（ローカルのコードベースを読み込み、構造的にファイル・関数・クラスなどをインデックス化している）

Anysphere Inc. が開発・提供。プランはHobby（無料）、Pro（$20/月）、Ultra（$200/月）がある。


<!--
**説明者ノート：**
- VSCodeユーザーには移行が簡単なことを強調
- AIが「追加機能」ではなく「中核」であることを説明
-->
---

## Cursorの基本情報

#### バージョン
- 2025年6月4日に最新バージョン：Cursor 1.0（正式版）リリース
- 最新版は2025年6月12日にアップデートされた1.1（7月1日時点）
#### GitHubスター数
Cursor の公式 GitHub リポジトリ（cursor/cursor）は 約30.6k スター
（OSSではないので、Issueの起票方法だけ載っている）

#### 利用者
2025年時点で、Cursor は 100万人を超えるユーザー を擁し、そのうち 約36万人が有料契約者

<!--
**説明者ノート：**
- 具体的な数字で説得力を持たせる
- 「乗り遅れない」という気持ちを喚起
-->

---

## Cursorができること

### 機能一覧

| カテゴリ | 機能 | 効果 |
|----------|------|------|
| **補完** | Tab補完 | コード記述を高速化 |
| **生成** | Ctrl+K、Composer | 新規実装を効率化 |
| **対話** | Chat、@記号 | 問題解決を迅速化 |
| **自動化** | Agent Mode | 作業を自動化 |
| **カスタマイズ** | Rules | 好みに最適化 |

VibeCodingにはAgentModeがおすすめ、コードの修正の効率化はTab補完などが効果的。

---

## 基本機能

---

## Tab補完

#### 機能概要
**AIが次に書くコードを予測して提案する機能**

#### 使い方
1. コードを書き始める
2. グレーの提案が表示される
3. `Tab`キーで採用 / `Esc`で却下

**💡 精度を上げるコツ：**
- 変数名を分かりやすくする
- コメントを書いてから実装
- 型定義を明確にする

<!--
**説明者ノート：**
- 実際にデモを見せると効果的
- Copilotとの違い（より文脈を理解）を説明
-->
---

## Tab補完の実例

### 実際の動作例

#### Python例
```python
def calculate_total(items):
    # アイテムの合計金額を計算
    # ここでTabを押すと...
    return sum(item.price * item.quantity for item in items)
```

#### JavaScript例
```javascript
const users = await fetchUsers();
// アクティブユーザーのみ抽出
// ここでTabを押すと...
const activeUsers = users.filter(user => user.isActive);
```

**🎯 ポイント：**
- コメントがヒントになる
- 変数名が明確だと精度UP
- パターンを学習して提案

**💡 活用シーン：**
- 定型的な処理
- エラーハンドリング
- テストコードの生成

<!--
**説明者ノート：**
- 実際の画面で動作を見せる
- 「魔法みたい」という感動を共有
-->
---

## Ctrl+K（Cmd+K）

### インラインコード生成

#### 🔧 機能概要
**選択範囲の書き換えや新規コード生成を行う機能**

#### できること
| 操作 | 説明 | 使用例 |
|------|------|---------|
| **書き換え** | 選択コードを変更 | リファクタリング |
| **生成** | 新規コード作成 | 関数の実装 |
| **変換** | 形式を変更 | Promise→async/await |

#### 基本操作
1. コード選択（または空行にカーソル）
2. `Ctrl+K`（Mac: `Cmd+K`）
3. 日本語で指示を入力
4. Enter で実行

**⚡ 時短テクニック：** よく使う指示は辞書登録しておく

<!--
**説明者ノート：**
- 「書き換え」が特に便利なことを強調
- 自然な日本語で指示できることをアピール
-->
---

## Ctrl+Kの実例 - 関数実装

### ゼロから関数を生成

#### 指示例
```
Ctrl+K: ユーザーの年齢から世代を判定する関数を作成。
        Z世代、ミレニアル世代、X世代、ベビーブーマー世代に分類
```

#### 生成結果
```python
def get_generation(age):
    """年齢から世代を判定する
    
    Args:
        age (int): ユーザーの年齢
        
    Returns:
        str: 世代名
    """
    if age < 20:
        return "Z世代"
    elif age < 40:
        return "ミレニアル世代"
    elif age < 55:
        return "X世代"
    else:
        return "ベビーブーマー世代"
```

**💡 良い指示のポイント：**
- 具体的な要件を含める
- 期待する出力を明確に
- 必要に応じて例を示す

<!--
**説明者ノート：**
- 指示の書き方で結果が変わることを説明
- 複雑な要件も理解できることを示す
-->
---

## Ctrl+Kの実例 - リファクタリング

### 既存コードの改善

#### Before（選択してCtrl+K）
```javascript
// 指示: より読みやすくリファクタリング。早期リターンを使用
if (user.age >= 18) {
    if (user.hasLicense) {
        if (car.isAvailable) {
            return true;
        }
    }
}
return false;
```

#### After
```javascript
// 年齢チェック
if (user.age < 18) {
    return false;
}

// 免許チェック
if (!user.hasLicense) {
    return false;
}

// 車の利用可能性チェック
return car.isAvailable;
```

**🎯 リファクタリングのコツ：**
- 「読みやすく」「保守しやすく」などの指示
- デザインパターンの適用も可能
- パフォーマンス改善の提案も

<!--
**説明者ノート：**
- コードの品質向上に使えることを強調
- チームでのコードレビューにも活用可能
-->
---

## Chat（Ctrl+L）

### AIとの対話

#### 💬 機能概要
**コードに関する質問や相談ができる対話型AI機能**

#### 特徴
- **会話形式**: 自然な言葉で質問
- **コンテキスト保持**: 会話の流れを理解
- **コード提案**: 実装案を提示

#### よくある使い方
| 用途 | 質問例 |
|------|--------|
| エラー解決 | 「このエラーの原因は？」 |
| 設計相談 | 「この機能の最適な実装方法は？」 |
| 学習 | 「このコードの動作を説明して」 |

**💡 効果的な質問方法：**
- エラーメッセージは全文貼る
- 背景や目的を説明する
- 具体的な制約条件を伝える

<!--
**説明者ノート：**
- 「先輩エンジニアに相談する感覚」と説明
- 恥ずかしい質問でもOKなことを強調
-->
---

## Chatの実例 - エラー解決

### エラーメッセージを貼るだけ

#### 質問例
```
このエラーの解決方法を教えてください：
TypeError: Cannot read property 'map' of undefined
   at UserList.render (UserList.js:15:23)
```

#### AIの回答
```markdown
このエラーは配列がundefinedの時にmapを呼んでいます。

**解決方法：**

1. デフォルト値を設定
   const items = data?.items || [];
   
2. 条件付きレンダリング
   {items && items.map(...)}
   
3. オプショナルチェーン
   {items?.map(...)}

**推奨：** オプショナルチェーンが最もシンプルです。
```

**🎯 エラー解決のコツ：**
- スタックトレース全体を貼る
- 関連コードも一緒に送る
- 試したことを伝える

<!--
**説明者ノート：**
- エラーで詰まった時の強い味方
- 初心者の「つまづき」を減らせる
-->
---

## @記号の活用

### コンテキストを指定

#### 🎯 機能概要
**AIに参照してほしいファイルやコードを明示的に指定する機能**

#### @の種類
| 記号 | 説明 | 使用例 |
|------|------|---------|
| `@ファイル名` | 特定ファイルを参照 | @user.py |
| `@Folders` | フォルダを参照 | @components |
| `@Code` | シンボルを参照 | @getUserData |
| `@Codebase` | プロジェクト全体 | プロジェクト構造の説明 |
| `@Docs` | ドキュメント検索 | React公式ドキュメント |
| `@Web` | Web検索 | 最新情報の取得 |

**使い方：** Chat内で`@`を入力して選択

**💡 活用のコツ：**
- 複数ファイルの整合性チェック
- プロジェクト全体の理解
- 最新情報の取得

<!--
**説明者ノート：**
- @を使うことで精度が格段に上がる
- 特に@Codebaseは便利
-->
---

## @Filesの実例

### 複数ファイルを考慮

#### シナリオ
```
@user.py @database.py @auth.py
これらのファイルを参照して、ユーザー登録機能を実装してください。
既存の認証システムと整合性を保つようにしてください。
```

#### AIの対応
```python
# 既存のインポートとパターンに従う
from database import get_db_connection
from auth import hash_password, generate_token
from user import User, UserSchema

async def register_user(email: str, password: str):
    """既存の認証システムに準拠したユーザー登録"""
    # 既存のバリデーションルールを適用
    user = UserSchema(email=email)
    
    # auth.pyの既存関数を使用
    hashed_pw = await hash_password(password)
    
    # database.pyのパターンに従う
    async with get_db_connection() as db:
        # ... 実装続く
```

**🎯 メリット：**
- 既存コードとの一貫性
- 車輪の再発明を防ぐ
- チーム規約の遵守

<!--
**説明者ノート：**
- 複数ファイルの関係性を理解することを強調
- 大規模プロジェクトで特に有効
-->
---

## @Codebaseの実例

### プロジェクト全体の理解

#### 質問例
```
@Codebase
このプロジェクトのアーキテクチャを説明してください。
主要なコンポーネントと、それらの関係を教えてください。
```

#### AIの分析結果
```
## プロジェクト構造

**アーキテクチャ：** MVCパターン + Repository層

### 主要コンポーネント：
- `models/`: データモデル定義（SQLAlchemy）
- `views/`: UIコンポーネント（React）
- `controllers/`: ビジネスロジック
- `repositories/`: データアクセス層

### 技術スタック：
- Backend: Django 4.0 + DRF
- Frontend: React 18 + TypeScript
- Database: PostgreSQL
- Cache: Redis

### データフロー：
View → Controller → Repository → Model → DB
```

**💡 活用シーン：**
- 新規参画時の理解
- リファクタリング計画
- ドキュメント作成

<!--
**説明者ノート：**
- プロジェクトの「地図」として使える
- 新メンバーのオンボーディングに最適
-->
---

## @Docsの実例

### ドキュメント参照

#### 使用例
```
@Docs React hooks
useEffectのクリーンアップ関数の正しい使い方を教えてください。
メモリリークを防ぐ方法も含めて。
```

#### 回答
```javascript
// 正しいクリーンアップの実装
useEffect(() => {
  // 1. イベントリスナーの場合
  const handleScroll = () => console.log('scrolling');
  window.addEventListener('scroll', handleScroll);
  
  // 2. タイマーの場合
  const timer = setTimeout(() => {
    console.log('Timer fired');
  }, 1000);
  
  // 3. 非同期処理のキャンセル
  const controller = new AbortController();
  
  // クリーンアップ関数
  return () => {
    window.removeEventListener('scroll', handleScroll);
    clearTimeout(timer);
    controller.abort();
  };
}, []);
```

**🎯 メリット：**
- 公式ドキュメントに基づく正確な情報
- ベストプラクティスの学習
- 最新APIの確認

<!--
**説明者ノート：**
- 「調べる時間」を大幅に削減
- 正確な情報源からの回答
-->
---

## @Webの実例

### 最新情報の取得

#### 活用シーン
```
@Web Next.js 15 新機能
App Routerでの並列ルートの実装方法を教えてください。
実践的な例も含めて。
```

#### 得られる情報
```typescript
// Next.js 15の並列ルート実装例
// app/layout.tsx
export default function Layout({
  children,
  team,
  analytics
}: {
  children: React.ReactNode
  team: React.ReactNode
  analytics: React.ReactNode
}) {
  return (
    <>
      {children}
      <div className="flex">
        <div className="w-1/2">{team}</div>
        <div className="w-1/2">{analytics}</div>
      </div>
    </>
  )
}
```

**💡 使いどころ：**
- 最新バージョンの機能
- トレンドの技術
- 解決策の検索

<!--
**説明者ノート：**
- ChatGPTの知識カットオフを超える情報
- 最新のベストプラクティスを学べる
-->
---

## Composerモード

### マルチファイル編集

#### 🎨 機能概要
**複数ファイルを同時に作成・編集できる高度な生成機能**

#### 特徴
| 機能 | 説明 | メリット |
|------|------|----------|
| **同時編集** | 複数ファイルを一括変更 | 整合性確保 |
| **新規作成** | ファイル群を一括生成 | 機能実装が高速 |
| **リファクタ** | 大規模な構造変更 | 安全な変更 |

#### アクセス方法
- ショートカット: `Ctrl+I`（Mac: `Cmd+I`）
- または画面右上のComposerアイコン

**🎯 使いどころ：**
- 新機能の実装（複数ファイル必要）
- 大規模リファクタリング
- テストコードの一括生成

<!--
**説明者ノート：**
- Ctrl+Kの上位版として説明
- デモで威力を見せる
-->
---

## Composerの実例

### 新機能の実装

#### 指示例
```
ユーザープロフィール編集機能を追加してください：
- RESTful APIエンドポイント（PUT /api/users/{id}/profile）
- Reactのフォームコンポーネント（バリデーション付き）
- 型定義ファイル
- 単体テストとE2Eテスト
```

#### 生成されるファイル
```
✅ api/users/profile.py      # APIエンドポイント
✅ components/ProfileForm.tsx # Reactコンポーネント  
✅ types/userProfile.ts      # TypeScript型定義
✅ validators/profile.py      # バリデーションロジック
✅ tests/test_profile.py      # APIテスト
✅ tests/ProfileForm.test.tsx # コンポーネントテスト
✅ e2e/profile.spec.ts       # E2Eテスト
```

**💡 成功のコツ：**
- 要件を明確に記述
- ファイル構成を指定
- 既存の規約を伝える

<!--
**説明者ノート：**
- 「一気に実装が進む感覚」を伝える
- 品質も高いことを強調
-->
---

## Agent Mode

### 背景での自動処理

#### 🤖 機能概要
**バックグラウンドでタスクを自動実行するAI機能**

#### 特徴
| 特性 | 説明 | 利点 |
|------|------|------|
| **非同期実行** | 他の作業をしながらAIが作業 | 並行作業可能 |
| **複数タスク** | 調査、修正、ドキュメント作成 | 包括的な対応 |
| **プロジェクト理解** | 全体を把握した上で作業 | 質の高い成果 |

#### 使用シーン
- 大量のリファクタリング
- レガシーコードの調査
- テスト網羅性の向上
- ドキュメントの自動生成

**⚡ 新機能：** Background Agentとして実装

<!--
**説明者ノート：**
- 「アシスタントを雇う」イメージで説明
- 非同期で動くことの価値を強調
-->
---

## Agent Modeの実例

### バックグラウンド実行

#### 指示例
```
Agent: このプロジェクトのすべてのTypeScriptエラーを調査し、
修正計画を立ててください。私は他の機能開発を続けます。
```

#### Agentの作業内容
```
🔍 実行中...
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✓ TypeScriptエラー検出: 24件
✓ 影響範囲の分析: 8ファイル  
✓ 修正優先度の設定: 完了
✓ 修正案の作成: 進行中... 75%
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[10分後]
📋 修正計画レポート:
- 型定義の不整合: 12件（優先度: 高）
- null安全性: 8件（優先度: 中）
- 未使用import: 4件（優先度: 低）
```

**💡 活用のコツ：**
- 明確なゴールを設定
- 進捗の確認方法を決める
- 結果の活用方法を考える

<!--
**説明者ノート：**
- 時間のかかる作業を任せられる
- 自分は創造的な作業に集中できる
-->
---

## Rulesとは

### AIの振る舞いをコントロール

#### 📏 機能概要
**プロジェクトや個人の開発規約をAIに学習させる機能**

#### Rulesの目的
| 目的 | 説明 | 効果 |
|------|------|------|
| **規約の自動適用** | コーディング規約を徹底 | 品質向上 |
| **一貫性確保** | チーム開発の統一 | レビュー負荷軽減 |
| **個人の好み** | 自分のスタイルを反映 | 快適な開発 |

#### 設定できること
- コードスタイル（インデント、命名規則）
- アーキテクチャパターン
- エラーハンドリング方針
- コメントの書き方
- テストの書き方

**🎯 本質：** AIを「自分専用」にカスタマイズ

<!--
**説明者ノート：**
- 「AIの教育」というイメージで説明
- チーム開発での価値を強調
-->
---

## Rules階層構造

### 3つのレベル

```
┌─────────────────┐
│  Custom Rules   │ ← タスク特有（一時的）
├─────────────────┤
│ Project Rules   │ ← プロジェクト共通
├─────────────────┤
│  User Rules     │ ← 個人設定（永続的）
└─────────────────┘
```

#### 優先順位
**Custom > Project > User**

#### 各レベルの説明
| レベル | 場所 | 用途 | 例 |
|--------|------|------|-----|
| **User** | ~/.cursor/rules | 個人の好み | 日本語コメント |
| **Project** | .cursor/rules | チーム規約 | 命名規則 |
| **Custom** | Composerで指定 | 特定タスク | 移行作業 |

**💡 使い分けのコツ：**
- 個人的な好み → User Rules
- チーム共通 → Project Rules  
- 一時的な作業 → Custom Rules

<!--
**説明者ノート：**
- 階層構造の意味を明確に
- 実際のファイルパスも示す
-->
---

## User Rulesの設定例

### 個人の好みを反映

#### 設定ファイル: `~/.cursor/rules`
```yaml
# 私のコーディングスタイル
general:
  language: japanese  # 日本語でコメント
  style:
    - 変数名は分かりやすく具体的に
    - 早期リターンを優先
    - ネストは2段階まで
    - エラーは必ず処理

language_specific:
  python:
    - Type hintsを必ず使用
    - docstringはGoogle形式
    - f-stringsを使用
    
  javascript:
    - constを優先、letは必要時のみ
    - アロー関数を使用
    - async/awaitを使用（Promiseより優先）
    
code_review:
  - 可読性を最優先
  - DRY原則に従う
  - テストを必ず書く
```

**🎯 効果：**
- どのプロジェクトでも自分のスタイル
- AIが好みを学習
- ストレスフリーな開発

<!--
**説明者ノート：**
- 実際に設定ファイルを見せる
- 日本語で書けることをアピール
-->
---

## Project Rulesの実例

### チーム開発での統一

#### `.cursor/rules` （プロジェクトルート）
```yaml
# チーム開発ルール
team_conventions:
  git:
    - コミットメッセージは英語
    - feat/fix/refactorプレフィックス使用
    - PRには必ずテストを含める
    
architecture:
  - Clean Architectureに従う
  - DIコンテナを使用
  - Repository patternで実装
  
api_design:
  - RESTful原則を遵守
  - エラーレスポンスはRFC 7807形式
  - ページネーションは必須

security:
  - 入力値は必ず検証
  - SQLインジェクション対策必須
  - 機密情報は環境変数へ
  - XSS対策を実装

testing:
  - カバレッジ80%以上
  - E2Eテストも作成
  - モックは最小限に
```

**💡 メリット：**
- 新メンバーもすぐに規約遵守
- コードレビューの負荷軽減
- 品質の自動担保

<!--
**説明者ノート：**
- Gitで管理できることを強調
- チーム全体の生産性向上
-->
---

## Rules実例1

### コーディング規約の徹底

#### Rule設定
```yaml
coding_standards:
  functions:
    - 単一責任の原則に従う
    - 関数は20行以内
    - 引数は3つまで
    
  nesting:
    - ネストは3段階まで
    - 早期リターンで平坦化
    
  naming:
    - 変数名は役割を表す
    - 略語は避ける
    - キャメルケース使用
```

#### 適用結果
```python
# AIが生成するコード
def process_order(order_data: OrderData) -> OrderResult:
    """注文を処理する（20行以内）"""
    # 早期リターンで検証
    if not order_data.is_valid():
        return OrderResult.invalid()
        
    # 関数を分割して単一責任に
    validated_data = _validate_order(order_data)
    payment_result = _process_payment(validated_data)
    shipping_info = _arrange_shipping(validated_data)
    
    return OrderResult(
        order_id=validated_data.id,
        payment=payment_result,
        shipping=shipping_info
    )

# プライベート関数に分割される
def _validate_order(data: OrderData) -> ValidatedOrder:
    # バリデーションロジック
    pass
```

**🎯 ポイント：** AIが自動的に規約を守る！

<!--
**説明者ノート：**
- 自動的にクリーンなコードになる
- レビュー指摘が減る効果
-->
---

## Rules実例2

### セキュリティ考慮の自動化

#### Rule設定
```yaml
security_rules:
  database:
    - SQLクエリは必ずプレースホルダ使用
    - ORMを優先的に使用
    
  user_input:
    - すべての入力をサニタイズ
    - 型チェックを実施
    
  authentication:
    - パスワードは必ずハッシュ化
    - bcryptまたはargon2使用
    
  api:
    - 認証にはJWT使用
    - CORS設定を明示
```

#### 生成されるコード
```python
from werkzeug.security import generate_password_hash
from flask_jwt_extended import create_access_token
import bleach

@app.route('/api/register', methods=['POST'])
def register_user():
    # 入力値のサニタイズ（自動追加）
    email = bleach.clean(request.json.get('email', ''))
    password = request.json.get('password', '')
    
    # 入力検証（自動追加）
    if not validate_email(email):
        return jsonify({'error': 'Invalid email'}), 400
        
    # パスワードのハッシュ化（自動適用）
    hashed_password = generate_password_hash(
        password,
        method='pbkdf2:sha256'
    )
    
    # プレースホルダを使用（自動適用）
    query = "INSERT INTO users (email, password) VALUES (?, ?)"
    db.execute(query, (email, hashed_password))
    
    # JWT生成（規約通り）
    access_token = create_access_token(identity=email)
    return jsonify({'token': access_token}), 201
```

**⚠️ 効果：** セキュリティホールを作りにくい

<!--
**説明者ノート：**
- セキュリティは後付けしにくい
- 最初から考慮されるメリット
-->
---

## Rules実例3

### テストコード生成の標準化

#### Rule設定
```yaml
testing_rules:
  structure:
    - すべての関数にユニットテスト作成
    - テストはAAA形式（Arrange-Act-Assert）
    - 1テスト1アサーション原則
    
  coverage:
    - 正常系・異常系・境界値
    - エッジケースを必ず含める
    
  naming:
    - test_[関数名]_[条件]_[期待結果]
    
  mocking:
    - 外部依存は必ずモック
    - モックは最小限に
```

#### 生成されるテスト
```python
import pytest
from unittest.mock import Mock, patch

def test_calculate_discount_正常系_割引額を返す():
    # Arrange
    original_price = 1000
    discount_rate = 0.2
    
    # Act
    result = calculate_discount(original_price, discount_rate)
    
    # Assert
    assert result == 800

def test_calculate_discount_境界値_ゼロ割引():
    # Arrange
    original_price = 1000
    discount_rate = 0
    
    # Act
    result = calculate_discount(original_price, discount_rate)
    
    # Assert  
    assert result == 1000

def test_calculate_discount_異常系_負の価格():
    # Arrange
    original_price = -100
    discount_rate = 0.2
    
    # Act & Assert
    with pytest.raises(ValueError, match="価格は正の数である必要があります"):
        calculate_discount(original_price, discount_rate)

@patch('payment.external_api')
def test_process_payment_外部API_モック使用(mock_api):
    # Arrange
    mock_api.charge.return_value = {'status': 'success'}
    
    # Act
    result = process_payment(1000, 'card_token')
    
    # Assert
    assert result.is_successful
    mock_api.charge.assert_called_once()
```

**💡 効果：** テストの質が自動的に向上

<!--
**説明者ノート：**
- テストの書き方に悩まない
- カバレッジも自然に上がる
-->
---

## Rules実例4

### ドキュメント生成の自動化

#### Rule設定
```yaml
documentation_rules:
  functions:
    - すべての公開関数にdocstring必須
    - Google Style Guide形式
    - 引数・戻り値・例外を明記
    
  examples:
    - 使用例を1つ以上含める
    - エッジケースの説明
    
  language:
    - 日本語で記述
    - 専門用語は英語併記
    
  updates:
    - コード変更時に同期更新
    - 古い情報は削除
```

#### 生成されるドキュメント
```python
def fetch_user_data(
    user_id: int, 
    include_details: bool = False,
    timeout: float = 30.0
) -> dict:
    """
    ユーザーデータを取得する
    
    指定されたユーザーIDに基づいて、データベースから
    ユーザー情報を取得します。詳細情報の取得は
    オプションで指定可能です。
    
    Args:
        user_id (int): ユーザーID（1以上の整数）
        include_details (bool, optional): 
            詳細情報を含めるか。デフォルトはFalse。
            Trueの場合、プロフィール詳細や統計情報も取得。
        timeout (float, optional): 
            タイムアウト秒数。デフォルトは30.0秒。
    
    Returns:
        dict: ユーザー情報を含む辞書
            {
                'id': int,
                'name': str,
                'email': str,
                'created_at': str,
                'details': dict  # include_details=Trueの場合のみ
            }
    
    Raises:
        UserNotFoundError: 指定されたユーザーが存在しない場合
        DatabaseConnectionError: DB接続エラーが発生した場合
        TimeoutError: タイムアウトした場合
    
    Example:
        >>> # 基本的な使用例
        >>> user = fetch_user_data(123)
        >>> print(user['name'])
        'John Doe'
        
        >>> # 詳細情報を含める場合
        >>> user_with_details = fetch_user_data(
        ...     user_id=123,
        ...     include_details=True
        ... )
        >>> print(user_with_details['details']['last_login'])
        '2024-01-15T10:30:00Z'
    
    Note:
        - user_idが0以下の場合はUserNotFoundErrorが発生
        - 大量のユーザー取得にはbatch_fetch_users()を推奨
        - キャッシュは5分間有効
    """
```

**📝 メリット：** ドキュメント作成の負担が激減

<!--
**説明者ノート：**
- ドキュメントが自動で最新に保たれる
- 他の開発者にも優しいコード
-->
---

## Awesome Cursor Rules

### コミュニティの知恵を活用

#### 🌟 GitHubリポジトリ
**https://github.com/PatrickJS/awesome-cursorrules**

#### 人気のRules例

| Rules名 | 内容 | おすすめ度 |
|---------|------|------------|
| **clean-code** | クリーンコードの原則 | ⭐⭐⭐ |
| **react-best-practices** | React開発のベストプラクティス | ⭐⭐⭐ |
| **python-zen** | Pythonの禅に従った開発 | ⭐⭐ |
| **security-first** | セキュリティ重視の開発 | ⭐⭐⭐ |
| **tdd-rules** | テスト駆動開発 | ⭐⭐ |

#### 使い方
1. リポジトリから選ぶ
2. `.cursor/rules`にコピー
3. 必要に応じてカスタマイズ

**💡 選び方のコツ：**
- スター数とメンテナンス状況を確認
- 自分の技術スタックに合うものを選ぶ
- まずは1つから始める

<!--
**説明者ノート：**
- コミュニティの力を借りられる
- 車輪の再発明を避けられる
-->
---

## Rulesのベストプラクティス

### 効果的なRules設定のコツ

#### ✅ DO - 推奨事項
| 項目 | 説明 | 例 |
|------|------|-----|
| **具体的に書く** | 曖昧な表現を避ける | ❌「良いコード」<br>✅「関数は20行以内」 |
| **段階的に導入** | 少しずつ増やす | 最初は3-5個のルール |
| **チームで議論** | 合意形成が重要 | 定例でルール見直し |
| **定期的に見直し** | プロジェクトに合わせて更新 | 3ヶ月ごとに棚卸し |

#### ❌ DON'T - 避けるべきこと
| 項目 | 理由 | 改善策 |
|------|------|---------|
| **抽象的すぎる指示** | AIが解釈に迷う | 数値や具体例を使う |
| **矛盾するルール** | 動作が不安定に | 優先順位を明確に |
| **過度な制約** | 創造性を阻害 | バランスを考慮 |

**🎯 成功の秘訣：** まず3個の重要なルールから始めて、徐々に洗練させる

<!--
**説明者ノート：**
- 完璧を求めすぎない
- PDCAサイクルで改善
-->
---

## Cursor 1.0アップデート概要

### AIとの共同開発を進化させる

#### 🚀 主要な新機能（2024年12月リリース）

| 機能 | 概要 | インパクト |
|------|------|------------|
| **BugBot** | GitHub PR自動レビュー | レビュー時間50%削減 |
| **Memories** | プロジェクト情報の記憶 | コンテキスト理解向上 |
| **Multi-Cursor (MCP)** | AI支援マルチカーソル | 一括編集の効率化 |
| **Background Agent** | 非同期タスク実行 | 並行作業が可能に |

#### 🎨 その他の改善
- Jupyter Notebook統合
- リッチなChat応答（Mermaid図）
- VS Code拡張機能の同期
- パフォーマンス向上

**💡 設計思想：** 「AIが開発者の意図を理解し、協働する」

*出典: Cursor 1.0 リリース記事*

<!--
**説明者ノート：**
- 大型アップデートの意義を説明
- 各機能の実用性を強調
-->
---

## BugBot

### GitHub PR自動レビュー

#### 🐛 機能概要
**プルリクエストを自動的に分析し、潜在的な問題を発見する機能**

#### できること
| 項目 | 内容 | 例 |
|------|------|-----|
| **バグ検出** | 潜在的な問題を発見 | null参照、メモリリーク |
| **改善提案** | より良い実装を提案 | パフォーマンス最適化 |
| **規約チェック** | コーディング規約の確認 | 命名規則、フォーマット |

#### 動作例
```markdown
🤖 BugBot Review

## ⚠️ 潜在的な問題:
- **L23**: `user.profile.settings`でnullチェックが不十分
  ```js
  // 修正案
  const settings = user?.profile?.settings || defaultSettings;
  ```

- **L45**: useEffectのクリーンアップ関数が未実装
  ```js
  useEffect(() => {
    const timer = setInterval(update, 1000);
    return () => clearInterval(timer); // 追加必要
  }, []);
  ```

## ✅ 改善提案:
- Optional chainingの使用を推奨
- エラーバウンダリの追加を検討
```

**💡 メリット：** レビュアーの負担軽減＆品質向上

<!--
**説明者ノート：**
- 人間のレビューを補完する存在
- 見逃しがちな問題を発見
-->
---

## Memories

### プロジェクト情報の記憶

#### 🧠 機能概要
**プロジェクトの文脈や過去の決定事項を記憶し、一貫性のある提案を行う機能**

#### 記憶する内容
| カテゴリ | 内容 | 活用場面 |
|----------|------|----------|
| **アーキテクチャ** | 設計方針、パターン | 新機能実装時 |
| **規約** | コーディングルール | コード生成時 |
| **技術スタック** | 使用ライブラリ、バージョン | 依存関係管理 |
| **過去の会話** | 重要な決定事項 | 継続的な開発 |

#### 活用例
```
💭 Memories が記憶していること:

1. このプロジェクトはClean Architectureを採用
2. 状態管理にはRedux Toolkitを使用
3. テストはJestとReact Testing Library
4. APIはGraphQLで実装
5. 前回の相談: パフォーマンス最適化について
   → React.memoとuseMemoの使い分けを議論
```

**🎯 効果：** 毎回同じ説明が不要に！

<!--
**説明者ノート：**
- 「AIが文脈を覚えている」安心感
- 長期プロジェクトで特に有効
-->
---

## Multi-Cursor (MCP)

### 複数箇所同時編集の進化

#### 🎯 機能概要
**AIが類似パターンを認識し、複数箇所を賢く同時編集する機能**

#### 従来との違い
| 項目 | 従来のマルチカーソル | AI支援MCP |
|------|---------------------|------------|
| **選択方法** | 手動で各箇所を選択 | AIが類似箇所を提案 |
| **編集内容** | 同じ内容を入力 | 文脈に応じて変更 |
| **スコープ認識** | なし | 変数スコープを理解 |

#### 使用例
```javascript
// 変数名の一括変更（スコープを考慮）
function processUser(usr) {  // usr → user
  const usrName = usr.name;  // usrName → userName
  const usrAge = usr.age;    // usrAge → userAge
  
  // 別スコープのusrは変更されない
  items.forEach(usr => {     // このusrは維持
    console.log(usr);
  });
}
```

**💡 活用シーン：**
- リファクタリング
- 命名規則の統一
- パターンの一括適用

<!--
**説明者ノート：**
- 「賢い」マルチカーソルであることを強調
- デモで違いを見せる
-->
---

## その他の新機能

### 開発体験の向上

#### 📊 Jupyter Notebook統合
```python
# データ分析コードの自動生成
@Code このデータを分析して可視化してください
```
- グラフ作成支援
- 分析コードの最適化
- 結果の解釈提案

#### 💬 リッチなChat応答
- **Mermaid.js図表**: フローチャートやER図を自動生成
- **コードハイライト**: より見やすい表示
- **段階的説明**: 複雑な概念を分解して説明

#### ⚙️ 設定・ダッシュボード改善
- より直感的なUI
- 使用統計の可視化
- チーム設定の簡素化

#### 🚀 パフォーマンス向上
- 起動時間: **50%短縮**
- メモリ使用量: **30%削減**
- レスポンス速度: **2倍高速化**

<!--
**説明者ノート：**
- 細かい改善の積み重ねも重要
- 日々の開発体験が向上
-->
---

## Privacy Mode

### 機密情報の保護

#### 🔒 機能概要
**コードがクラウドに送信されないローカル実行モード**

#### Privacy Modeとは
| 項目 | 通常モード | Privacy Mode |
|------|------------|--------------|
| **データ送信** | クラウドへ送信 | ローカルのみ |
| **処理場所** | リモートサーバー | ローカルマシン |
| **対応モデル** | すべて | 一部制限あり |

#### 有効化方法
1. 設定 → Privacy
2. "Privacy Mode"をON
3. 必要に応じてファイル単位で設定

#### 使用シーン
- 🏢 顧客データを扱うコード
- 🔐 社内システムの開発  
- 💡 特許申請前のアルゴリズム
- 💰 金融・医療系のシステム

**⚠️ 注意点：** 一部の高度な機能は制限される

<!--
**説明者ノート：**
- セキュリティ重視の企業でも安心
- 柔軟な設定が可能
-->
---

## モデルの選び方ガイド

### 用途別おすすめモデル

#### 🎯 基本方針
```
速度重視 → GPT-4o
品質重視 → Claude 3.5 Sonnet  
バランス → Gemini 2.5 Pro
```

#### 詳細な使い分け

| 用途 | 推奨モデル | 理由 |
|------|------------|------|
| **単純な補完** | GPT-4o | 高速レスポンス |
| **複雑なロジック** | Claude 3.5 | 推論力が高い |
| **多言語対応** | Gemini 2.5 | 幅広い知識 |
| **長文生成** | Claude 3.5 | 一貫性が高い |
| **リファクタリング** | Claude 3.5 | コード理解力 |
| **ドキュメント作成** | Gemini 2.5 | 構造化が得意 |

**💡 切り替えのコツ：**
- タスクごとに最適なモデルを選択
- 応答速度と品質のバランスを考慮
- コストも意識して選択

<!--
**説明者ノート：**
- モデルの特徴を理解して使い分ける
- デフォルトはGPT-4oで十分なことが多い
-->
---

## モデル比較表

### 性能・特徴比較

| モデル | 速度 | 品質 | コスト | 得意分野 |
|--------|------|------|--------|----------|
| **GPT-4o** | ⚡⚡⚡ | ⭐⭐⭐ | $ | 汎用・高速処理 |
| **Claude 3.5 Sonnet** | ⚡⚡ | ⭐⭐⭐⭐⭐ | $$ | 複雑な推論・長文 |
| **Claude 4** | ⚡⚡ | ⭐⭐⭐⭐⭐ | $$$ | 最高品質（制限あり） |
| **Gemini 2.5 Pro** | ⚡⚡⚡ | ⭐⭐⭐⭐ | $ | マルチモーダル |

#### 🔄 切り替え方法
チャット画面上部のモデル選択ボタンから変更

#### 💰 コスト目安（月間）
- 軽度使用（補完中心）: $5-10
- 中度使用（生成も活用）: $15-30  
- 重度使用（常時利用）: $30-50

**📊 使用統計：** ダッシュボードで確認可能

<!--
**説明者ノート：**
- コストパフォーマンスを意識
- 用途に応じた使い分けが重要
-->
---

## Cursorの内部構成

### なぜ速いのか

#### ⚙️ 技術的な工夫

```
ユーザー入力
    ↓
[ローカルインデックス] ← 事前解析済み
    ↓
[コンテキスト構築] ← 必要最小限
    ↓  
[最適化されたプロンプト]
    ↓
[並列API呼び出し] ← 複数モデル同時
    ↓
[ストリーミング応答] ← 逐次表示
```

#### 🚀 キーポイント

| 技術 | 説明 | 効果 |
|------|------|------|
| **ローカルインデックス** | コードベースを事前解析 | 検索高速化 |
| **差分同期** | 変更部分のみ送信 | 通信量削減 |
| **キャッシュ活用** | 類似リクエストを記憶 | レスポンス向上 |
| **並列処理** | 複数処理を同時実行 | 待ち時間短縮 |

**💡 結果：** VSCode + AIプラグインより体感速度が速い

<!--
**説明者ノート：**
- 技術的な優位性を簡潔に説明
- 「サクサク動く」理由を理解してもらう
-->
---

## トラブルシューティング

### よくある問題と解決法

#### 🔧 症状別対処法

| 症状 | 原因 | 解決方法 |
|------|------|----------|
| **補完が遅い** | モデル負荷 | • モデルをGPT-4oに変更<br>• キャッシュクリア |
| **提案が的外れ** | コンテキスト不足 | • Rulesを見直す<br>• @でファイル指定 |
| **エラーが発生** | 拡張機能競合 | • Cursor再起動<br>• 拡張機能を確認 |
| **料金が高い** | 使いすぎ | • 使用モデルの見直し<br>• Privacy Mode活用 |

#### 🆘 それでも解決しない場合
1. 公式ドキュメントを確認
2. コミュニティフォーラムで質問
3. GitHubでIssue報告

**💡 予防のコツ：**
- 定期的にアップデート
- 拡張機能は最小限に
- ログを確認する習慣

<!--
**説明者ノート：**
- トラブル時も慌てない
- 大抵の問題には解決策がある
-->
---

## AI開発ツール全体マップ

### 各ツールの立ち位置

```
        高自律性
           ↑
    Devin  |  Agent Mode
           |    (Cursor)
    Cline  |  
           |  Cursor
           |  Claude Code
  Copilot  |
           |
        低自律性
    シンプル ← → 高機能
```

#### 📊 ツールの特徴

| ツール | 自律性 | 機能性 | 主な用途 |
|--------|--------|--------|----------|
| **Copilot** | 低 | 中 | コード補完 |
| **Cursor** | 中 | 高 | 統合開発環境 |
| **Claude Code** | 中 | 中 | 対話型開発 |
| **Cline** | 高 | 中 | 自動化タスク |
| **Devin** | 最高 | 高 | 完全自動開発 |

**🎯 Cursorの強み：** バランスの良さ

<!--
**説明者ノート：**
- 各ツールには適材適所がある
- Cursorは「ちょうどいい」位置
-->
---

## 機能比較表

### 主要AI開発ツール比較

| 機能 | Cursor | Copilot | Claude Code | Cline | Devin |
|------|--------|---------|-------------|-------|-------|
| **IDE統合** | ◎ | ◎ | ○ | △ | × |
| **対話機能** | ◎ | △ | ◎ | ○ | ◎ |
| **自律動作** | ○ | × | △ | ○ | ◎ |
| **マルチファイル** | ◎ | △ | ○ | ◎ | ◎ |
| **カスタマイズ** | ◎ | △ | ○ | ○ | △ |
| **価格** | $$ | $ | $$ | Free | $$$ |

◎:優秀 ○:対応 △:限定的 ×:非対応

#### 💡 選択基準
- **統合開発環境が欲しい** → Cursor
- **VSCodeから離れたくない** → Copilot
- **対話しながら開発** → Claude Code
- **自動化重視** → Cline/Devin

<!--
**説明者ノート：**
- 表を見ながら特徴を解説
- Cursorの万能性を強調
-->
---

## 自走度と人の介在度

### どこまでAIに任せるか

#### 🤖 ツール別の特徴
```
人の介在度: 高 ← → 低
Copilot → Cursor → Claude Code → Cline → Devin

タスクサイズ: 小 ← → 大
行単位 → 関数単位 → ファイル単位 → 機能単位 → プロジェクト
```

#### 使い分けマトリックス

| 介在度 | タスクサイズ | 適したツール | 使用例 |
|--------|------------|--------------|---------|
| **高** | 小 | Copilot | 日常のコーディング |
| **中** | 中 | **Cursor** | 機能実装・デバッグ |
| **中** | 中 | Claude Code | ペアプログラミング |
| **低** | 大 | Cline | 定型作業の自動化 |
| **最低** | 最大 | Devin | プロトタイプ作成 |

**🎯 Cursorの立ち位置：** 人とAIの協調

<!--
**説明者ノート：**
- 完全自動化が必ずしも良いわけではない
- 制御と効率のバランスが重要
-->
---

## 適材適所

### ツールの使い分け指針

#### 🎯 シーン別おすすめ

| シーン | おすすめ | 理由 |
|--------|----------|------|
| **日常のコーディング** | **Cursor** | 高速補完＋必要時に対話 |
| **ペアプログラミング** | Claude Code | 対話しながら開発 |
| **定型作業の自動化** | Cline | スクリプト的な処理 |
| **新規開発の丸投げ** | Devin | 要件から実装まで |
| **既存IDEを変えたくない** | Copilot | プラグインとして導入 |

#### 💼 組織での導入指針
```
個人開発者 → Cursor（コスパ最高）
小規模チーム → Cursor Business
大企業 → Copilot（既存環境維持）
研究開発 → Devin（実験的利用）
```

**🔄 併用もアリ：** Cursor + Copilotなど

<!--
**説明者ノート：**
- 正解は1つではない
- 状況に応じて使い分ける柔軟性
-->
---

## 本日のまとめ

### Cursorで変わる開発体験

#### ✅ 学んだこと
- **基本機能**（Tab、Ctrl+K、Chat、@記号）
- **Rulesによるカスタマイズ** - AIを自分専用に
- **Cursor 1.0の新機能** - さらなる効率化
- **実践的な活用方法** - プロ級の使い方
- **他ツールとの使い分け** - 適材適所

#### 🚀 次のアクション
| タイミング | アクション | 目標 |
|------------|------------|------|
| **今日** | Cursorをインストール | 環境構築 |
| **今週** | 基本機能を使ってみる | Tab補完マスター |
| **来週** | Rulesを設定してみる | 自分好みに |
| **来月** | チームに展開を検討 | 生産性向上 |

### 💪 Let's start AI-powered coding!

**最後のメッセージ：** AIは怖くない、強い味方です！

<!--
**説明者ノート：**
- 参加者の背中を押す
- 質問タイムへ移行
-->
---

# 参考リンク

### 公式リソース
- **Cursor公式**: https://cursor.com
- **Cursor Docs**: https://docs.cursor.com  
- **Cursor Forum**: https://forum.cursor.com

### コミュニティ
- **Awesome Cursor Rules**: https://github.com/PatrickJS/awesome-cursorrules
- **Reddit r/cursor**: 実践的なTips共有
- **YouTube**: Cursor公式チャンネル


---

## おつかれさまでした！
次はハンズオンです！