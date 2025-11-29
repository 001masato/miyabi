# Intent Resolution Framework - 意図解決フレームワーク

**Version**: 1.0.0
**Last Updated**: 2025-11-07
**Concept**: Intent → Goal → Tasks → Execution

---

## 🎯 概要

**Intent Resolution Framework**は、ユーザーの曖昧な意図を、実行可能なタスクに変換し、最終的な目標達成まで導く完全なフレームワーク。

### 核心プロセス

```
[Input] → [User Intent] → [Fixed Goal] → [Tasks] → [Agent Execution] → [Result]
```

---

## 📐 数学的定義

### Step-Back Question Formula（ステップバック質問公式）

```
F(Achieve Goal using Step-Back Question) = A to Z = ∫F(step) = Result

Where:
  F(Goal) = 目標達成関数
  A to Z = 完全なプロセス（開始から完了まで）
  ∫F(step) = 各ステップの積分（累積実行）
  Result = 最終成果物
```

**意味**:
- 目標達成は、個別のステップの累積（積分）である
- 各ステップを問い直す（step-back）ことで、最適な経路を見つける
- A（開始）からZ（完了）まで、連続的な変換プロセス

---

## 🔄 完全な実行フロー

### Phase 1: Intent Capture（意図捕捉）

```
[Input] → [User Intent] → [Intent Analysis]

Intent = {
  explicit_intent: ユーザーが明示的に述べた要求,
  implicit_intent: 文脈から推測される暗黙の意図,
  want_intent: ユーザーが本当に欲しいもの,
  need_intent: ユーザーが実際に必要なもの
}
```

### Phase 2: Intent Disambiguation（意図明確化）

```
[Intent Analysis] → [Step-Back Questions] → [Fixed Goal]

Step-Back Questions:
  Q1: "なぜこれが必要なのか？" (Why)
  Q2: "何を達成したいのか？" (What)
  Q3: "どのような状態が理想か？" (How)
  Q4: "制約条件は何か？" (Constraints)
```

### Phase 3: Goal Decomposition（目標分解）

```
[Fixed Goal] → [Task Decomposition] → [Task List]

Goal = ∑(Task₁, Task₂, ..., Task_n)

Task Decomposition Process:
  1. Goal Analysis: 目標を構成要素に分解
  2. Dependency Mapping: タスク間の依存関係を特定
  3. Priority Assignment: 優先順位の割り当て
  4. Resource Estimation: 必要なリソース見積もり
```

### Phase 4: Task Execution（タスク実行）

```
[Task List] → [Agent Assignment] → [Execution Loop] → [Result]

For each Task in Task List:
  1. Select Agent: 適切なAgentを選択
  2. Generate Prompt: タスク実行用のプロンプト生成
  3. Assign Tool: 必要なツールを割り当て
  4. Execute: Agentがタスクを実行
  5. Feedback: 結果を検証
  6. Loop: 次のタスクへ or 再実行
```

---

## 🔗 フレームワーク統合

### Intent Resolution × World Model Logic

```
[Phase 1: Intent Capture] = θ₁ Understand
  Input → Intent → Understanding
  World₀における意図の認識

[Phase 2: Intent Disambiguation] = θ₂ Generate (Part 1)
  Step-Back Questions → Fixed Goal
  明確な目標の生成

[Phase 3: Goal Decomposition] = θ₂ Generate (Part 2) + θ₃ Allocate
  Fixed Goal → Tasks → Agent Assignment
  実行計画の生成とリソース割り当て

[Phase 4: Task Execution] = θ₄ Execute + θ₅ Integrate + θ₆ Learn
  Tasks → Execution Loop → Result → Learning

  各Task実行 = 1回の「瞬き」:
    World₀ → Task₁ → World₁ → Task₂ → World₂ → ... → World_n
```
