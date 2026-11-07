# [UIM04] ユーザー操作メニュー

Figma で開く: [`user_actions` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91509)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `user_actions` | [4:91509](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91509) | [4:91573](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91573) | [4:91558](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91558) | [4:91622](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91622) |
| `user_actions_muted` | [39:8084](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-8084) | [39:8158](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-8158) | [39:8135](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-8135) | [39:8209](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-8209) |

## 概要

機能目的:

- 他の利用者に対して、ブロック・ミュート・通報を選んでもらう

機能概要:

- 対象の利用者の表示
- ブロック・ミュート・通報への導線

関連する機能：D-03、H-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 対象の利用者を表示する |
| 2 | ブロックする | ボタン押下 | [UIM05](../UIM05/README.md) を起動 |
| 3 | ミュートする | ボタン押下 | [UIM06](../UIM06/README.md) を起動 |
| 4 | 通報する | ボタン押下 | [UIS45](../UIS45/README.md) へ遷移 |
| 5 | 閉じる | リンク押下 | メニューを閉じる |
| 6 | 対象のプロフィール | 項目押下 | [UIS23](../UIS23/README.md)（`user_posts`）へ遷移 |
| 7 | ミュートを解除する | ボタン押下 | ミュートを解除し、メニューを閉じる（ミュートしている利用者だけ） |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | プロフィール欄 | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| 全状態 | ブロックする | [UIM05](../UIM05/README.md)（`block_confirm`） | モーダルを起動 |
| `user_actions` | ミュートする | [UIM06](../UIM06/README.md)（`mute_confirm`） | モーダルを起動 |
| `user_actions_muted` | ミュートを解除する | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| 全状態 | 通報する | [UIS45](../UIS45/README.md)（`report_form`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| user_name | 対象の利用者のユーザー名 | |

利用API：なし（呼び出し元の [UIS23](../UIS23/README.md) が取得したプロフィールを使う）

画面表示制御:

- PC では「その他」のボタンの右側に小さく開くメニュー（ポップオーバー）で表示する
- ここではブロック・ミュートを実行しない
- ミュートしている利用者の場合は、「ミュートする」の代わりに「ミュートを解除する」を表示する（`user_actions_muted`）

### 4. 通報する

[UIS45](../UIS45/README.md) へ遷移する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| target_type | `user` | |
| target_id | 対象の利用者の ID | |

### 5. 閉じる

メニューを閉じる。背景の一覧と、見ていた位置は保つ。

### 7. ミュートを解除する

確認を出さずにミュートを解除し、メニューを閉じる。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API60 | ミュートを解除する | user_name |

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
