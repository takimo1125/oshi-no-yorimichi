# [UIS34] 週末便メールの配信停止

Figma で開く: [`mail_unsubscribe` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110006)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `mail_unsubscribe` | [19:110006](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110006) | [19:110054](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110054) | [19:110042](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110042) | [19:110084](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110084) |

## 概要

機能目的:

- 週末便メールの配信停止のリンクから来た人に、ログインしなくても配信を止めてもらう

機能概要:

- 週末便メールの配信停止
- 通知の設定への導線

関連する機能：A-03、F-03

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | リンクが有効かを確かめ、停止前の確認を表示する |
| 2 | 配信を停止する | ボタン押下 | 週末便メールを停止し、同じ画面で完了の表示に切り替える |
| 3 | 変更しない | ボタン押下 | [UIS01](../UIS01/README.md) へ遷移 |
| 4 | 通知の設定へ | リンク押下 | [UIS33](../UIS33/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 変更しない | [UIS01](../UIS01/README.md)（`lp`） | 画面へ遷移 |
| 全状態 | 通知の設定へ | [UIS33](../UIS33/README.md)（`notification_settings`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| unsubscribe_token | メールのリンクに含まれる値 | 誰の配信を止めるかを特定する。利用者の ID と用途を HMAC で署名した値 |

画面表示制御:

- 未ログインのヘッダーを使う
- リンクが無効な場合の表示は未確定

### 2. 配信を停止する

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API23 | 週末便メールの受信をオフにする | unsubscribe_token |

画面表示制御:

- 停止に成功したら、同じ画面で完了の表示に切り替える
- アカウントやほかの通知の設定は変えない

### 4. 通知の設定へ

[UIS33](../UIS33/README.md) へ遷移する。未ログインの場合は [UIS05](../UIS05/README.md) を経由する。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
