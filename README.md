# Qiitadon 酒場<sup>β</sup>

Qiitadon 酒場は旧 Qiitadon メンバーが集うチャットルームです。

> みんなの引越し先はこちら: [github.com/Qiitadon/welcome](https://github.com/Qiitadon/welcome/blob/main/README.md)

## 目指すもの

- 静的ページによるメンバー限定のチャット・ルーム
  - Javascript + HTML5 + プライベート IPFS による、静的ページで構成されているサーバーレスな P2P 型のチャットルーム。
  - [公開 IPFS によるデモ](https://ipfs.io/ipfs/bafybeia5f2yk6td7ciroeped2uwfivo333b524t3zmoderfhl3xn7wi7aa/) （別ブラウザで開いて試してみてください。【注意】: 公開 IPFS なので Qiitadon 民以外も参加できます）
- 可能なら
  - 各々が住んでいるインスタンスの OAuth でログインできる（表示名取得用）
  - チャットルームの投稿は、まず自身のインスタンスのホームに非公開で投稿されてからチャットルームに流れる。
  - UI を Qiitadon に近しいものにする。

## TODO

- [x] Organization 作成: [https://github.com/Qiitadon](https://github.com/Qiitadon)
- [x] ドメイン取得: [https://qiitadon.fans/](https://qiitadon.fans/)
- [x] プライベート IPFS の Bootstrap 用ノード（起動時の初回問い合わせ先のピア）の準備
  - [x] ネットワーク・キーの作成（`~/.ipfs/swarm.key`）
  - [x] VPS でのプライベート IPFS の動作確認
  - [x] RaspberryPi Zero でのプライベート IPFS の動作確認
  - [x] Docker でのプライベート IPFS の動作確認
- [ ] IPFS のバックアップ用クラスターの準備
  - [x] クラスター・キーの作成（`cluster-secret`）
  - [x] VPS のバックアップ・クラスターのの動作確認
  - [x] RaspberryPi Zero でのバックアップ・クラスターの動作確認
  - [ ] Docker でのプライベート IPFS の動作確認
- [ ] 静的 IPFS チャットルームの設置
   - [ ] [デモ](https://ipfs.io/ipfs/bafybeia5f2yk6td7ciroeped2uwfivo333b524t3zmoderfhl3xn7wi7aa/)をベースに叩き台設置
   - [ ] `js-ipfs` による `swarm.key` の設定方法確認
- [ ] K3S による Kubernetes クラスターのマスター・ノードの準備
   - [ ] K3S ベースの Minecraft サーバ設置

## 引越し・バックアップツール

- [MastoOwn](https://hidao80.github.io/MastoOwn/)
  - アクセストークンと期間を指定すれば 5,000 件ごとに JSON ファイルとしてダウンロードできる。
  - HTML と JavaScript だけで作られた完全な静的サイトなので安心。
- [NoteStock](https://notestock.osa-p.net/)
  - 自分の過去のトゥートを検索できる。
  - 複数インスタンスのアカウントと連携（グループを作成）しておけば、サーバーが終了しても検索できる。（らしい。未確認）

