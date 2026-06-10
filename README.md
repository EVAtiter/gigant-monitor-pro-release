# Gigant Monitor Pro

**Gigant Monitor Pro** は、macOS のシステム状況を紫×黄の液体メーターで表現する
メニューバー常駐ユーティリティ「Gigant Monitor」の **上位版**です。
80 年代アニメ計器を思わせるアートワークで、システムの状態を「眺めて楽しむ」ツールです。

このリポジトリは **Gigant Monitor Pro（公証済みバイナリ）の配布窓口**です。
ソースコードは公開していません。

> 通常版「Gigant Monitor」は Mac App Store で配布しています（無料）。
> Pro 版は App Store では提供できない **消費電力メーター** を搭載した
> Developer ID 直接配布版です。

---

## 通常版との違い

| | Gigant Monitor（App Store） | Gigant Monitor Pro（このリポ） |
|---|---|---|
| CPU メーター | ✅ | ✅ |
| ネットワーク（下り / 上り） | ✅ | ✅ |
| **消費電力メーター** | ― | ✅（Apple Silicon） |
| 配布 | Mac App Store | 公証済みバイナリ（直接配布） |

消費電力メーターは Apple の非公開 API（IOReport）を使うため App Store 版には
搭載できません。Pro 版は Developer ID 署名 + Apple 公証済みで配布しています。

---

## ダウンロード

最新版は [Releases](https://github.com/EVAtiter/gigant-monitor-pro-release/releases/latest) から。

1. `Gigant-Monitor-Pro-<バージョン>.zip` をダウンロード
2. 解凍して `Gigant Monitor Pro.app` を `アプリケーション` フォルダーへ
3. 初回起動時に確認が出たら「開く」をクリック（公証済みなので Gatekeeper を通ります）

---

## 主な機能

- 4 つの独立メーター: CPU / 下り / 上り / **消費電力**
- 各メーターはサイズ・透明度・常時最前面・位置固定を個別に調整可能
- ネットワーク・電力は「直近 N 分のスライディングウィンドウ最大」を 100% として可視化
  （5 分 / 15 分 / 30 分 / 1 時間から選択）
- 整列メニュー（CPU の下／右／左に縦並び、初期リセット）
- 低電力モード（フレームレートを落として消費電力を抑制）
- マルチモニター環境ではディスプレイ別に位置を記憶
- 日本語 / 英語 UI 対応
- アプリ自身は外部通信を一切行いません

## 動作要件

- macOS 14.0 Sonoma 以降
- Universal binary（Apple Silicon / Intel 両対応）
  - 消費電力メーターは **Apple Silicon** でのみ動作します（Intel 機では非表示）

## プライバシー

Gigant Monitor Pro は **データを一切収集しません**。
計測値はすべてお使いの Mac 内で完結し、外部に送信されません。
詳細は通常版と共通の
[プライバシーポリシー](https://github.com/EVAtiter/gigant-monitor-support/blob/main/PRIVACY.md)
を参照してください。

## サポート

質問・要望・不具合報告は通常版と共通の窓口へ:

- [Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)
- [Issues](https://github.com/EVAtiter/gigant-monitor-support/issues)
