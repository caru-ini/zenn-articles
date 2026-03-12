# Alchemy 記事調査メモ

作成日: 2026-03-12
対象記事: `articles/96de2600acec67.md`

## この記事の狙い

- 「TypeScript でインフラを書きたい」「Cloudflare Workers をコードで扱いたい」層に刺さる導入記事にする
- Terraform / Pulumi / CDK と比較したときの Alchemy の気持ちよさを短く伝える
- 読後に 10 分以内で `bun alchemy dev` まで試せる短いハンズオンを入れる

## SEO 観点の仮説

### 主キーワード

- Alchemy
- TypeScript IaC
- Cloudflare Workers IaC
- Infrastructure as TypeScript

### 副キーワード

- Pulumi 代替
- Terraform 代替
- Cloudflare Workers デプロイ
- TypeScript でインフラを定義
- AWS Lambda IaC

### タイトル案

1. TypeScript だけで Cloudflare/AWS のインフラを書ける IaC「Alchemy」がかなり面白い
2. Terraform や Pulumi より軽い？ TypeScript ネイティブ IaC「Alchemy」を触ってみた
3. TypeScript でインフラを書く時代へ。Alchemy の思想と最短ハンズオン

### 見出しで拾いたい検索意図

- Alchemy とは何か
- 何が他の IaC と違うか
- Cloudflare Workers でどう使うか
- まず何から試せばいいか

## 面白さの軸

- 純粋な TypeScript / ESM で完結している
- リソースが `async function` ベースで、学習コストが低い
- State がローカル JSON で見える
- Cloudflare 周りのテンプレートやガイドが厚く、試すまでが速い
- AI で独自 Resource を作る思想がかなり前面に出ている
- Cloudflare 中心に見えるが AWS も触れられるので、遊びより実務に接続しやすい

## 逆に注意点

- 2026-03-12 時点でもかなり速いペースで更新されている
- 開発モードは docs 上で beta 表記あり
- Cloudflare の導線が特に強いので、まずは Cloudflare で試すのが自然
- Terraform 互換の巨大エコシステムをそのまま期待するものではない

## 記事構成案

1. はじめに
2. Alchemy とは
3. 何が面白いのか
4. どんな人に向いているか
5. 5 分ハンズオン
6. 使って感じた注意点
7. まとめ

## ハンズオン方針

Cloudflare Worker を 1 本デプロイする最短導線にする。

- `bun init -y`
- `bun add alchemy`
- `bun alchemy configure`
- `bun alchemy login`
- `alchemy.run.ts` と `src/worker.ts` を作る
- `bun alchemy dev`
- `bun alchemy deploy`
- 必要なら `bun alchemy destroy`

`alchemy create` もあるが、今回は「中身が見える最小構成」を優先する。

## 記事で押さえる一次情報

- GitHub リポジトリは 2026-03-12 時点で約 1.9k stars、96 forks、247 releases、直近リリースは 2026-03-11
- 公式ブログでは、Alchemy は pure TypeScript / ESM-native / async function / transparent state を差別化要因として説明している
- Getting Started では Cloudflare Worker を最初の題材にしている
- docs には Next.js / Nuxt / React Router / TanStack Start / Bun SPA などの Cloudflare 向けガイドがある
- GitHub README の examples には Cloudflare 系に加えて AWS Lambda の例もある

## 使う表現メモ

- 「TypeScript でインフラを書く」だけでなく「TypeScript がそのまま実行系になっている」に寄せる
- 「IaC の重さが薄い」「道具感が軽い」という言い回しは有効
- ただし Terraform / Pulumi を雑に下げず、「思想がかなり違う」に留める

## 参照元

- https://github.com/alchemy-run/alchemy
- https://alchemy.run/getting-started/
- https://alchemy.run/blog/2025-07-01-how-alchemy-is-different/
- https://alchemy.run/guides/cloudflare-worker/
- https://alchemy.run/concepts/dev/
