[English](README.md) | [日本語](README.ja.md)

# Gigant Monitor Plus

**Gigant Monitor Plus** は、macOS のシステム状況を紫×黄の液体メーターで表現する
メニューバー常駐ユーティリティ「Gigant Monitor」の **直接配布版**です。
70 年代アニメ計器を思わせるアートワークで、システムの状態を「眺めて楽しむ」ツールです。

このリポジトリは **Gigant Monitor Plus（公証済みバイナリ）の配布窓口**です。

> 通常版「Gigant Monitor」は [Mac App Store](https://apps.apple.com/app/gigant-monitor/id6777906549) で配布しています（無料）。
> Plus 版は、App Store 版のすべての機能に **消費電力の表示** を加えた、Developer ID の直接配布版です。
>
> v2.2.2 までの名前は「Gigant Monitor Pro」でした。v2.3.0 で「Gigant Monitor Plus」に変わりました（機能と設定はそのまま引き継がれます）。

---

## 通常版との違い

| | Gigant Monitor（App Store） | Gigant Monitor Plus（このリポ） |
|---|---|---|
| 液体メーター（CPU / ネットワーク / ディスク） | ✅ | ✅ |
| タイムライン（ネットワーク / ディスク） | ✅ | ✅ |
| CPU タイムライン | ✅ | ✅（電力・CPU タイムライン） |
| **消費電力メーター**（CPU ウィンドウで切り替え） | ― | ✅ |
| **電力・CPU タイムライン** | ― | ✅ |
| 配布 | Mac App Store | 公証済みバイナリ（直接配布） |

消費電力を読むには、App Store のサンドボックスでは使えない仕組み
（システム管理コントローラー SMC への直接アクセス）が要るため、App Store 版には搭載できません。
**消費電力に興味がなければ App Store 版で十分**です。

---

## ダウンロード

### Homebrew（推奨）

```sh
brew install --cask EVAtiter/tap/gigant-monitor-plus
```

> Homebrew が信頼していない tap として読み込みを拒否する場合は、
> 先に `brew trust --cask EVAtiter/tap/gigant-monitor-plus` を実行してください。
>
> 旧名の `gigant-monitor-pro` でインストールしている場合も、`brew upgrade` で自動的に移行されます。

### 手動

最新版は [Releases](https://github.com/EVAtiter/gigant-monitor-pro-release/releases/latest) から。

1. `Gigant-Monitor-Plus-<バージョン>.zip` をダウンロード
2. 解凍して `Gigant Monitor Plus.app` を `アプリケーション` フォルダーへ
3. 初回起動時に確認が出たら「開く」をクリック（公証済みなので Gatekeeper を通ります）

---

## 主な機能

- **3 つの液体メーター**: CPU / ネットワーク（上り・下り）/ ディスク（読み込み・書き込み）
- **消費電力メーター**（Plus 限定）: CPU ウィンドウの表示を「CPU 使用率 ↔ 消費電力」で切り替え。
  ノート型の Mac ではチップ（SoC）の電力、デスクトップ型の Mac では Mac 全体の電力を表示します
- **3 つのタイムライン**: 電力・CPU（Plus 限定。上段に CPU 使用率、下段に消費電力）/ ネットワーク / ディスク の推移を、
  なめらかな曲線の面で表示。右端が現在で、左へ流れていきます（既定はオフ）
  - ネットワークは中心線から上へ「上り」、下へ「下り」
  - ディスクは中心線から上へ「Read」、下へ「Write」
- **初期配置は指標ごとに 1 列**。液体メーターの真下に対応するタイムラインが並びます
- 10 種の配色テーマをメニューから切り替え。液体の色・液体の透明度・パネルの透明度も調整でき、
  テーマごとに設定を保持します
- 各ウィンドウはサイズ・位置固定を個別に設定。全ウィンドウ共通で
  「常に最前面」「壁紙に貼り付ける」を切り替え
- **画面下端で呼び出す**: 画面のいちばん下にマウスを 0.5 秒置くと、表示中のウィンドウを
  一時的に最前面へ（既定オフ）
- ネットワーク・ディスク・電力は「直近のピーク」を 100% として可視化
  （ピーク記憶時間は 5 分 / 15 分 / 30 分 / 1 時間 / 無制限 から選択）
- 整列メニュー（縦並び・横並び・初期リセット）
- 低電力モード（フレームレートを落として消費電力を抑制）。アイドル時は自動でフレームレートを下げ、
  画面スリープ中や他のウィンドウに完全に隠れている間は描画を止めます
- マルチモニター環境ではディスプレイ別に位置を記憶
- 日本語 / 英語 UI 対応
- アプリ自身は外部通信を一切行いません

## 動作要件

- macOS 14 Sonoma 以降
- Apple Silicon（arm64）専用
- Apple 公証済み（Notarized by Apple）

## プライバシー

Gigant Monitor Plus は **データを一切収集しません**。
計測値はすべてお使いの Mac 内で完結し、外部に送信されません。
詳細は通常版と共通の
[プライバシーポリシー](https://github.com/EVAtiter/gigant-monitor-support/blob/main/PRIVACY.md)
を参照してください。

## サポート

質問・要望・不具合報告は通常版と共通の窓口へ:

- [Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)
- [Issues](https://github.com/EVAtiter/gigant-monitor-support/issues)

---

Copyright © 2026 EVA Titer. All rights reserved.
