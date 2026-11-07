# [UIM13] 展示の削除の確認

Figma で開く: [`exhibition_delete_confirm` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11416)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `exhibition_delete_confirm` | [49:11416](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11416) | [49:11553](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11553) | [49:11440](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11440) | [49:11577](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11577) |

## 概要

機能目的:

- 展示を削除する直前に、本当に削除するかを確かめる

機能概要:

- 対象の展示の表示
- 元の記録は残ることの案内
- 展示の削除

関連する機能：E-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 対象の展示を表示する |
| 2 | 削除する | ボタン押下 | 展示を削除し、[UIS25](../UIS25/README.md) に戻る |
| 3 | キャンセル・閉じる | ボタン押下 | 何もせずにモーダルを閉じる |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 削除する | [UIS25](../UIS25/README.md)（`exhibitions`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| exhibition_id | 削除する展示の ID | |

利用API：なし（呼び出し元の [UIS25](../UIS25/README.md) が取得した展示を使う）

画面表示制御:

- 展示の表紙とタイトルを表示する
- 展示を削除しても、元の記録は残ることを示す

### 2. 削除する

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API66 | 展示を削除する | exhibition_id |

画面表示制御:

- 削除に成功したら、モーダルを閉じて [UIS25](../UIS25/README.md) の一覧を表示し直す。0 件になった場合は `exhibitions_empty` にする
- 本人が操作する削除と、契約の終了による扱いを区別する。契約が終わっても、展示を自動で削除しない（[展示数と契約終了後の操作](../UIS25/README.md#展示数と契約終了後の操作)）

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
