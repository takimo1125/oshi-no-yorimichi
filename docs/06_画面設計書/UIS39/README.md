# [UIS39] 展示プラスの申し込み内容の確認

Figma で開く: [`billing_checkout_handoff` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98659)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `billing_checkout_handoff` | [4:98659](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98659) | [4:98750](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98750) | [4:98730](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98730) | [4:98831](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98831) |

## 概要

機能目的:

- 申し込む前に、このサービスの画面でプランの内容を確かめてもらい、Stripe の申し込み画面（Stripe Checkout）へ進んでもらう

機能概要:

- 展示プラスの料金と機能の表示
- 契約の条件（特定商取引法に基づく表記・利用規約）への導線
- Stripe Checkout への移動

関連する機能：G-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | Stripeの申し込み画面へ | ボタン押下 | 申し込みを始め、Stripe Checkout へ移動 |
| 3 | プランの案内へ戻る | ボタン押下 | [UIS38](../UIS38/README.md) へ遷移 |
| 4 | 契約の条件 | リンク押下 | [UIS48](../UIS48/README.md)・[UIS46](../UIS46/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 特定商取引法に基づく表記 | [UIS48](../UIS48/README.md)（`commerce`） | 画面へ遷移 |
| 全状態 | 利用規約 | [UIS46](../UIS46/README.md)（`terms`） | 画面へ遷移 |
| 全状態 | プランの案内へ戻る | [UIS38](../UIS38/README.md)（`plus_inactive`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API：なし

画面表示制御:

- カードの入力欄は、このサービスでは作らない。支払い方法は Stripe の画面で入力してもらう
- 申し込み前に [展示プラスの契約条件](../UIS38/README.md#展示プラスの契約条件) を表示する。決定済みの条件を法務本文・Stripe の設定と揃える。表示への反映が済んでいない箇所は、仮の条件で補わない

### 2. Stripeの申し込み画面へ

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API76 | 有効な契約や確認中の申し込みがないことを確かめ、Stripe Checkout のセッションを作る | なし |

画面表示制御:

- 作ったセッションの URL へ移動する
- すでに有効な契約がある場合は [UIS38](../UIS38/README.md)、確認中の申し込みがある場合は [UIS40](../UIS40/README.md) へ遷移し、二重に申し込ませない
- Stripe で申し込みを終えて戻ってきたら [UIS40](../UIS40/README.md) を表示する。申し込みを中断して戻ってきた場合も [UIS40](../UIS40/README.md)（中断した状態）を表示する

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
