# [UIS42] 契約情報の確認

Figma で開く: [`billing_portal_return` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99401)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `billing_portal_return` | [4:99401](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99401) | [4:99458](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99458) | [4:99438](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99438) | [4:99486](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99486) |
| `billing_cancel_pending` | [4:99595](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99595) | [4:99652](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99652) | [4:99637](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99637) | [4:99685](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99685) |
| `billing_cancel_scheduled` | [39:6835](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6835) | [39:6904](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6904) | [39:6878](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6878) | [39:6938](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6938) |

## 概要

機能目的:

- カスタマーポータルから戻ってきた人に、手続きの後の契約の状態を伝える

機能概要:

- 契約の状態の取得と、状態に合わせた画面への振り分け
- 解約の反映を待っている状態と、解約の予約を確認できた状態の表示

関連する機能：G-01、G-02

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 契約の状態を取得し、状態に合わせて遷移する |
| 2 | 状況を確認する | ボタン押下 | 同じ契約の状態を取得し直す |
| 3 | 設定へ戻る | ボタン押下 | [UIS31](../UIS31/README.md) へ遷移 |
| 4 | 契約管理を開く | ボタン押下 | 解約の予約を確認できた状態で、[UIS41](../UIS41/README.md) へ遷移する |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 設定へ戻る | [UIS31](../UIS31/README.md)（`settings`） | 画面へ遷移 |
| `billing_cancel_pending` | 状況を確認する | 同じ画面（`billing_portal_return`） | 状態の切り替え |
| `billing_cancel_scheduled` | 契約管理を開く | [UIS41](../UIS41/README.md)（`billing_portal_handoff`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API75 | 本人の展示プラスの契約の状態と有料権限を取得する | なし |

画面表示制御:

| 契約の状態 | 遷移・表示 |
| --- | --- |
| 契約中（変更しなかった場合を含む） | [UIS38](../UIS38/README.md) へ遷移 |
| 支払い情報の確認が必要 | [UIS38](../UIS38/README.md)（支払い情報の確認が必要な状態）へ遷移 |
| 契約終了 | [UIS38](../UIS38/README.md)（契約終了の状態）へ遷移 |
| 解約の反映を確認中（API75 の `state` が `cancel_pending`） | 同じ画面で「解約手続きの状況を確認しています」を表示する（`billing_cancel_pending`） |
| 期間末の解約予約を確認済み（API75 の `state` が `cancel_scheduled`） | 同じ画面で「解約の予約を受け付けました」と、予約を取り消せることを表示する（`billing_cancel_scheduled`）。支払い済み期間の終了までは利用できる状態として、反映確認中と区別する |
| まだ確かめられない | 同じ画面で「契約情報を確認しています」を表示する（`billing_portal_return`） |

- 解約の反映を確認中の表示と、解約の予約を確認済みの表示に、終了する日付や残りの日数は出さない
- 解約の効力と返金は [契約条件](../UIS38/README.md#展示プラスの契約条件) に従う。解約予約だけで有料権限を直ちに終了させない
- 期間末の解約予約を確認済みの場合は、支払い済み期間の終了前なら予約を取り消せることを案内する。取消しの条件は [契約条件](../UIS38/README.md#展示プラスの契約条件) に従う。予約の取消しを確認できたら、契約中として [UIS38](../UIS38/README.md) へ遷移する
- カスタマーポータルから戻ったら、少し時間をおいて API75 を呼び直す
- 解約予約の取消しは、カスタマーポータルで行う（[UIS41](../UIS41/README.md)）。カスタマーポータルは、請求期間の終了まで解約の取消しに対応する（[Stripe の資料](https://docs.stripe.com/customer-management/configure-portal)）

### 2. 状況を確認する

イベント 1 と同じ API で、同じ契約の状態を取得し直す。二重に解約を求めたり、新しい申し込みを作ったりしない。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
