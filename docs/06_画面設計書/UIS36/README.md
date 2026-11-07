# [UIS36] 退会前の展示プラス契約の確認

Figma で開く: [`billing_withdraw_notice` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100132)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `billing_withdraw_notice` | [4:100132](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100132) | [4:100188](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100188) | [4:100176](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100176) | [4:100242](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100242) |

## 概要

機能目的:

- 展示プラスの契約中の人に、退会する前に契約の内容を確かめてもらう

機能概要:

- 契約の管理（Stripe のカスタマーポータル）への導線
- 退会の説明・設定への導線

関連する機能：A-04、G-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | 展示プラスの契約を確認する | ボタン押下 | [UIS41](../UIS41/README.md) へ遷移 |
| 3 | 退会の説明へ戻る | ボタン押下 | [UIS35](../UIS35/README.md) へ遷移 |
| 4 | 設定へ戻る | リンク押下 | [UIS31](../UIS31/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 展示プラスの契約を確認する | [UIS41](../UIS41/README.md)（`billing_portal_handoff`） | 画面へ遷移 |
| 全状態 | 退会の説明へ戻る | [UIS35](../UIS35/README.md)（`withdraw`） | 画面へ遷移 |
| 全状態 | 設定へ戻る | [UIS31](../UIS31/README.md)（`settings`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API：なし

画面表示制御:

- 解約を退会の条件にはしない。事前に解約しなくても、退会の受付時に次回の自動更新を停止する（[UIS35](../UIS35/README.md#3-退会する)）
- 「展示プラスの契約について」に、解約しなくても退会できること、退会の受付時に次回の自動更新を停止すること、支払い済み期間の日割り返金はしないこと、退会を取り消しても自動更新は再開しないことを示す

### 2. 展示プラスの契約を確認する

[UIS41](../UIS41/README.md) へ遷移する。契約の管理画面を開いただけでは、解約したとはみなさない。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
