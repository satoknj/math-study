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

*学習中*

---

## ③ 順伝播層（FFN）

*学習中*

---

## ④ 損失関数（Loss）

*学習中*

---

## ⑤ 学習（Backpropagation）

*学習中*
