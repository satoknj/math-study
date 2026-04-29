# LLM → 数学 マップ

LLM を構成する概念と、それが依拠する数学の対応図。
学習を進めながら徐々に詳細を追記していく。

---

## 全体像

```mermaid
graph TD
  LLM["LLM (Transformer)"]

  LLM --> EMB["① 埋め込み (Embedding)"]
  LLM --> ATT["② 注意機構 (Attention)"]
  LLM --> FFN["③ 順伝播層 (FFN)"]
  LLM --> LOSS["④ 損失関数 (Loss)"]
  LLM --> TRAIN["⑤ 学習 (Backpropagation)"]
```

---

## ① 埋め込み（Embedding）

```mermaid
graph TD
  EMB["埋め込み<br/>トークン → n次元空間上の点(ベクトル)"]
  EMB --> VS["ベクトル空間 (R^n)<br/>加算・スカラー倍が定義された空間"]

  VS --> AX["公理<br/>演算が信頼できることの保証<br/>→ Attention の加重和 w1*v1+...+wn*vn が成立する根拠"]
  VS --> LC["線形結合・基底・次元<br/>→ 埋め込みの次元数の意味<br/>→ 各次元が独立した特徴を表す"]
  VS --> NM["ノルム<br/>ベクトルの大きさ・距離<br/>→ 埋め込み間の類似度を測る基盤"]
```

---

## ② 注意機構（Attention）

```mermaid
graph TD
  ATT["注意機構 (Attention)<br/>処理中のトークンが他のトークンから関連情報を集める"]

  ATT --> QKV["Q・K・V の生成<br/>同じトークンのベクトル x から<br/>W_Q・W_K・W_V で用途別に変換"]

  QKV --> Q["Query (Q)<br/>問う側：今処理しているトークンが<br/>『何を知りたいか』を表す方向"]
  QKV --> K["Key (K)<br/>答える側の看板：参照されるトークンが<br/>『何を提供できるか』を表す方向"]
  QKV --> V["Value (V)<br/>答える側の中身：実際に渡す情報"]

  Q --> DOT["内積 <q, k><br/>QとKの方向の一致度 = 関連度<br/>= ||q||*||k||*cos(θ)"]
  K --> DOT

  DOT --> SM["Softmax<br/>スコアを確率（重み）に変換"]
  SM --> WS["加重和 (weighted sum)<br/>重み * v_1 + 重み * v_2 + ...<br/>= 線形結合"]
  V --> WS
```

#### 使われる数学

| 要素 | 数学 |
|---|---|
| Q・K・V の生成 | 行列・線形写像 |
| `<q, k>` | 内積（= ノルム × cos θ） |
| `/sqrt(d)` によるスケーリング | ノルム（分散の安定化） |
| Softmax | 指数関数・確率の正規化 |
| 加重和 | 線形結合 |

---

## ③ 順伝播層（FFN）

*学習中*

---

## ④ 損失関数（Loss）

*学習中*

---

## ⑤ 学習（Backpropagation）

*学習中*
