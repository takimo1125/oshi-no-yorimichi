# [UIS31] 設定

Figma で開く: [`settings` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-109852)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `settings` | [19:109852](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-109852) | [19:109924](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-109924) | [19:109911](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-109911) | [19:109993](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-109993) |

## 概要

機能目的:

- アカウントの設定の入口として、各設定の画面へ案内する

機能概要:

- プロフィール・通知・展示プラス・退会への導線
- ログイン方法（[UIS54](../UIS54/README.md)）への導線
- ブロック・ミュートした人の一覧への導線

関連する機能：A-02、A-03、A-04、G-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | プロフィール | ボタン押下 | [UIS32](../UIS32/README.md) へ遷移 |
| 3 | 通知 | ボタン押下 | [UIS33](../UIS33/README.md) へ遷移 |
| 4 | 展示プラス | ボタン押下 | [UIS38](../UIS38/README.md) へ遷移 |
| 5 | 退会について | リンク押下 | [UIS35](../UIS35/README.md) へ遷移 |
| 6 | ログイン方法 | ボタン押下 | [UIS54](../UIS54/README.md) へ遷移し、ログイン方法を追加・解除する |
| 8 | ブロック・ミュートした人 | ボタン押下 | [UIS53](../UIS53/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | プロフィール | [UIS32](../UIS32/README.md)（`profile_edit`） | 画面へ遷移 |
| 全状態 | 通知 | [UIS33](../UIS33/README.md)（`notification_settings`） | 画面へ遷移 |
| 全状態 | 展示プラス | [UIS38](../UIS38/README.md)（`plus_inactive`） | 画面へ遷移 |
| 全状態 | ログイン方法 | [UIS54](../UIS54/README.md)（`auth_methods`） | 画面へ遷移 |
| 全状態 | ブロック・ミュートした人 | [UIS53](../UIS53/README.md)（`blocked_muted_users`） | 画面へ遷移 |
| 全状態 | アカウント | [UIS35](../UIS35/README.md)（`withdraw`） | 画面へ遷移 |
| 全状態 | 退会について | [UIS35](../UIS35/README.md)（`withdraw`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API：なし

### 4. 展示プラス

[UIS38](../UIS38/README.md) へ遷移する。契約の状態による表示の切り替えは [UIS38](../UIS38/README.md) で行う。ただし、申し込みの確認中の場合は [UIS40](../UIS40/README.md) へ遷移する。

### 6. ログイン方法

[UIS54](../UIS54/README.md) へ遷移する。認証方式の追加・解除は UIS54 で行う。

### 8. ブロック・ミュートした人

[UIS53](../UIS53/README.md) へ遷移する。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
