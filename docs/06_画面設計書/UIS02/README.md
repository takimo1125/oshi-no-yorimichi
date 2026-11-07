# [UIS02] 新規登録

Figma で開く: [`signup` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=16-108092)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `signup` | [16:108092](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=16-108092) | [16:108143](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=16-108143) | [16:108128](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=16-108128) | [16:108173](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=16-108173) |

## 概要

機能目的:

- 登録の方法（Google 連携かメールアドレス）を選んでもらう

機能概要:

- Google 連携での登録への導線
- メールアドレスでの登録への導線
- ログインへの導線

関連する機能：A-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | Googleで続ける | ボタン押下 | Google の認証を経て [共通分岐](../UIS05/README.md#google-認証後の共通分岐) に従う |
| 3 | メールアドレスで登録する | リンク押下 | [UIS04](../UIS04/README.md) へ遷移 |
| 4 | ログイン | リンク押下 | [UIS05](../UIS05/README.md) へ遷移 |
| 5 | 利用規約・プライバシーポリシー | リンク押下 | [UIM01](../UIM01/README.md) を起動 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 利用規約 | [UIM01](../UIM01/README.md)（`terms_modal`） | モーダルを起動 |
| 全状態 | プライバシーポリシー | [UIM01](../UIM01/README.md)（`privacy_modal`） | モーダルを起動 |
| 全状態 | Googleで続ける | [UIS03](../UIS03/README.md)（`signup_profile`） | 画面へ遷移 |
| 全状態 | メールアドレスで登録する | [UIS04](../UIS04/README.md)（`signup_email`） | 画面へ遷移 |
| 全状態 | ログイン | [UIS05](../UIS05/README.md)（`login`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API：なし

### 2. Googleで続ける

Google の認証画面へ移動する。認証に成功して戻ったら、登録の入口からでも [UIS05 の共通分岐](../UIS05/README.md#google-認証後の共通分岐) に従う。Google の認証画面はこのサービスでは作らない。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API06 | Google の認証を始める | `mode=signup`、return_to |

画面表示制御:

- 認証を中断した・失敗した場合は、`google_error=1` を付けて戻る。表示は未確定
- Figma のリンクは未登録の利用者が [UIS03](../UIS03/README.md) へ進む例。登録・Google 連携済みの場合に、登録情報を再入力させない

### 5. 利用規約・プライバシーポリシー

[UIM01](../UIM01/README.md) を起動する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| document | `terms` または `privacy` | 表示する文書 |
| caller | `UIS02` | 閉じたときの戻り先 |

## 未確定事項

- Google 認証の中断・失敗時の表示はイベント 2 を参照。メールで登録済みの利用者と同じメールアドレスの場合は [UIS05 の共通分岐](../UIS05/README.md#google-認証後の共通分岐) に従う
