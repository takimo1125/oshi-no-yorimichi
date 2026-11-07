# [UIM11] グッズの削除の確認

Figma で開く: [`goods_delete_confirm` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7050)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `goods_delete_confirm` | [39:7050](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7050) | [39:7093](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7093) | [39:7074](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7074) | [39:7117](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7117) |

## 概要

機能目的:

- グッズを削除する直前に、本当に削除するかと、記録への影響を確かめる

機能概要:

- 対象のグッズの表示
- 記録は残ることの案内
- グッズの削除

関連する機能：B-04

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 対象のグッズを表示する |
| 2 | 削除する | ボタン押下 | グッズを削除し、[UIS18](../UIS18/README.md) へ遷移 |
| 3 | キャンセル・閉じる | ボタン押下 | 何もせずにモーダルを閉じ、[UIS21](../UIS21/README.md) に戻る |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 削除する | [UIS18](../UIS18/README.md)（`goods_list`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| goods_id | 削除するグッズの ID | |

利用API：なし（呼び出し元の [UIS21](../UIS21/README.md) が取得したグッズを使う）

画面表示制御:

- グッズの写真と名前を表示する
- グッズを削除しても記録は残り、記録とグッズの結び付きだけを外すことを示す

### 2. 削除する

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API45 | グッズを削除する | goods_id |

画面表示制御:

- グッズを削除しても、記録は残す。記録とグッズの結び付きだけを外す
- 削除に成功したら [UIS18](../UIS18/README.md) へ遷移する

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
