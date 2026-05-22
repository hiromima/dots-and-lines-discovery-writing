# dots-and-lines-discovery-writing

A Claude Skill for **discovery-driven writing** — place the dots, let the reader draw the line.

「点を配置して、線は受け手に引かせる」原理に基づき、学習・変容を目的とした文章・プレゼンテーションの構成を設計する Claude Skill です。

---

## このスキルでできること

ワークショップ台本、登壇台本、解説記事、チュートリアルなど **「受け手に発見してほしい」文書**の構成を設計します。

- **結論先出し型ではない構成**: 結論を最後に「立ち上げる」設計
- **意図的な穴の配置**: 受け手の質問を誘導する「さそいこみ」
- **予定→実行→結果サイクル**: 受け手の頭の中でサイクルを高速で回す

意思決定が目的の文書（提案書、契約書、ガイドライン本体など）には**絶対に発動しない**ガード付き。

## 思想的出典

このスキルは以下の方々の発信を起源・基礎としています：

- **濱村崇氏（[@GDLab_Hama](https://x.com/GDLab_Hama)）** — ハル研究所出身ゲームデザイナー。本スキルの中核3原理（点と線・さそいこみ・予定実行結果サイクル）すべての出典
- **ニカイドウレンジ氏（[@R_Nikaido](https://x.com/R_Nikaido)）** — 「知識アンロックの自分で気付けた感」概念

詳細は [`references/origin.md`](./references/origin.md) を参照してください。

## 使い方

### Claude Desktop の場合

1. [Releases](https://github.com/hiromima/dots-and-lines-discovery-writing/releases) から `.skill` ファイルをダウンロード
2. Claude Desktop を起動
3. 設定 → スキル管理 → インポート
4. ダウンロードした `.skill` ファイルを選択

### Claude Code の場合

```bash
cd ~/.claude/skills/
git clone https://github.com/hiromima/dots-and-lines-discovery-writing.git
```

または、プロジェクト単位で使う場合：

```bash
cd /path/to/your/project
mkdir -p .claude/skills
cd .claude/skills
git clone https://github.com/hiromima/dots-and-lines-discovery-writing.git
```

## 使用例

```
「○○について新人デザイナー向けの90分ワークショップ台本を作って」
「カンファレンスの30分の登壇台本を、結論先出しじゃなく組んで」
「note記事の構成を、最後に気づきが立ち上がる形で組み立てて」
「点と線型で構成して」
```

これらのリクエストでスキルが起動します。

## 起動しない場面

以下には**絶対に発動しません**：

- ロゴデザインのプレゼン資料
- クライアント向け提案書（受注前の意思決定が目的）
- MOU・契約書・仕様書
- ブランドガイドライン本体
- API・技術ドキュメント
- 議事録・進捗報告・週次レポート

判定基準: **目的が「決定・実行」なら起動しない、「学習・変容・発見」なら起動する**

## ファイル構成

```
dots-and-lines-discovery-writing/
├── SKILL.md                          # スキル本体・中核原理・起動判断
├── templates/                        # 出力テンプレート
│   ├── workshop-script.md            # ワークショップ台本
│   ├── presentation-deck.md          # 登壇台本
│   ├── explainer-article.md          # 解説記事
│   └── tutorial.md                   # チュートリアル
└── references/                       # 詳細仕様・参考資料
    ├── origin.md                     # 思想的出典（重要）
    ├── decision-tree.md              # 起動判定の決定木
    ├── anti-patterns.md              # 10個のNGパターン
    ├── desktop-variant.md            # Claude Desktop環境用
    └── code-variant.md               # Claude Code環境用
```

## 制作背景

このスキルは、濱村崇氏のX投稿シリーズ（2026年5月）を読んだ前尾博己（[@enhanced_jp](https://x.com/enhanced_jp)）が、「ゲームデザイン理論をワークショップ・プレゼン構成に転用できないか」と考えて Claude と対話しながら作成しました。

ブランドアーキテクトとしての実務（特にワークショップ設計・登壇）で日常的に使われています。

## ライセンス

MIT License — 詳細は [LICENSE](./LICENSE) を参照

## クレジット

- スキル設計・実装: 前尾博己（[enhanced Inc.](https://enhanced-inc.com)）
- 中核原理: 濱村崇氏（[@GDLab_Hama](https://x.com/GDLab_Hama)）
- 関連概念: ニカイドウレンジ氏（[@R_Nikaido](https://x.com/R_Nikaido)）

## Contributing

改善提案・バグ報告は Issue または Pull Request でお願いします。
特に `references/anti-patterns.md` への追加事例は歓迎します。
