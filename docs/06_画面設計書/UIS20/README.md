# [UIS20] グッズの登録

Figma で開く: [`goods_create` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84634)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `goods_create` | [4:84634](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84634) | [4:84706](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84706) | [4:84686](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84686) | [4:84768](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84768) |

## 概要

機能目的:

- 持っているグッズを手入力で登録してもらう

機能概要:

- グッズの写真・名前・お迎え日・公式ページの URL の入力
- グッズの登録

関連する機能：B-04、F-04

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | 写真を選択してアップロード | ボタン押下 | 端末の写真を選び、アップロードする |
| 3 | 登録する | ボタン押下 | グッズを登録し、[UIS19](../UIS19/README.md) へ遷移 |
| 4 | キャンセル | ボタン押下 | 保存せずに [UIS18](../UIS18/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 登録する | [UIS19](../UIS19/README.md)（`goods_detail`） | 画面へ遷移 |
| 全状態 | キャンセル | [UIS18](../UIS18/README.md)（`goods_list`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| return_to | 元の画面 | [UIM02](../UIM02/README.md) から記録の作成・編集の途中で開いたとき。登録後、`picked_goods_id=<登録したグッズの ID>` を付けてこの画面へ戻る |

利用API：なし

### 2. 写真を選択してアップロード

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API24 | 画像 ID とアップロード用の URL を発行する | 1 枚 |

### 3. 登録する

入力チェック:

| 項目 | チェック |
| --- | --- |
| 写真 | 任意。1 枚 10MB まで。JPEG・PNG |
| グッズの名前 | 必須。50 文字まで |
| お迎え日 | 任意。日付であること |
| 公式ページの URL | 任意。URL の形式であること |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API44 | グッズを登録する | 入力フォームの値、画像 ID |

画面表示制御:

- 登録に成功したら [UIS19](../UIS19/README.md) へ遷移する
- Figma の登録後のリンクは [UIS19](../UIS19/README.md)、キャンセルは [UIS18](../UIS18/README.md) を示す。`return_to` があるときは、登録後に `picked_goods_id` を付けて `return_to` の画面へ戻る。記録の入力中の内容は sessionStorage から復元する（[API 設計書の「画面間の入力の受け渡し」](../../07_API設計書/README.md#画面間の入力の受け渡し)）

### 補足

- 商品検索・価格・数量の入力欄は設けない
- お迎え日は、お迎え記念日の通知（F-04）に使う

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
