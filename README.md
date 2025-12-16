# Multi-Agent Discussion 実験リポジトリ

Claude の sub-agent を活用して議論と意思決定を行う実験用リポジトリです。

## 概要

このリポジトリでは、システムのリアーキテクチャに関する技術選定を題材に、Claude の sub-agent を使った議論と、使わない議論を比較実験しています。

## 実験内容

### 議論テーマ

- どのような言語や技術スタックを選択すべきか
- どのような開発手法や理論を使えば保守性を向上させることができるか

### 背景シナリオ

10年以上の歴史を持つサービス（会員数900万人超）のバックエンドシステムを、PHP/CakePHP から再設計するというシナリオで議論を行います。

## ディレクトリ構成

```
.
├── README.md
├── prompt-multi-agent.md      # マルチエージェント版のプロンプト
├── prompt-no-agent.md         # エージェントなし版のプロンプト
└── disscussion-results/       # 議論結果の出力先
    ├── discussion-result-multi-agent-*.md
    └── discussion-result-no-agent-*.md
```

## 実験パターン

| パターン | 説明 |
|---------|------|
| multi-agent | Claude の sub-agent を活用して複数の視点から議論 |
| no-agent | sub-agent を使わずに単体で議論 |

## 使い方

1. `prompt-multi-agent.md` または `prompt-no-agent.md` の内容を Claude に入力
2. 議論結果が `disscussion-results/` ディレクトリに出力される

## 出力フォーマット

議論結果には以下の内容が含まれます：

1. 結論
2. 結論に対する簡単な説明（200文字程度）
3. 背景に記載がない前提
4. どのようなことが検討されたかの詳細
5. どのエージェントが使われたか（multi-agent版のみ）
