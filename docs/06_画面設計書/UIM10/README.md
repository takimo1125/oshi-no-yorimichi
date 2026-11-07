# [UIM10] 下書きの削除の確認

Figma で開く: [`draft_delete_confirm` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6964)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `draft_delete_confirm` | [39:6964](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6964) | [39:7007](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7007) | [39:6988](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-6988) | [39:7031](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=39-7031) |

## 概要

機能目的:

- 下書きを削除する直前に、本当に削除するかを確かめる

機能概要:

- 対象の下書きの表示
- 下書きの削除

関連する機能：B-06

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 対象の下書きを表示する |
| 2 | 削除する | ボタン押下 | 下書きを削除し、[UIS13](../UIS13/README.md) へ戻る |
| 3 | キャンセル・閉じる | ボタン押下 | 何もせずにモーダルを閉じる |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 削除する | [UIS13](../UIS13/README.md)（`drafts`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| draft_id | 削除する下書きの ID | |

利用API：なし（呼び出し元の [UIS13](../UIS13/README.md) が取得した下書きを使う）

画面表示制御:

- 下書きのタイトルと、写真がある場合は最初の写真を表示する

### 2. 削除する

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API28 | 下書きを削除する | draft_id |

画面表示制御:

- 削除に成功したら、モーダルを閉じて [UIS13](../UIS13/README.md) の一覧を表示し直す。下書きが 0 件になった場合は 0 件の表示にする（`drafts_empty`）

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
