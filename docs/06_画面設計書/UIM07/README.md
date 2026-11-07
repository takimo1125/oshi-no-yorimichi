# [UIM07] PDF 書き出しの確認

Figma で開く: [`export_pdf_request` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89430)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `export_pdf_request` | [4:89430](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89430) | [4:89484](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89484) | [4:89467](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89467) | [4:89521](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89521) |

## 概要

機能目的:

- 展示プラスの契約者に、展示を印刷用の PDF にする依頼をしてもらう

機能概要:

- 書き出す展示の表示（タイトル・記録の件数・期間）
- PDF の作成の依頼

関連する機能：E-06

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 有料権限を確かめ、書き出す展示を表示する |
| 2 | PDF を作成する | ボタン押下 | PDF の作成を依頼し、[UIS44](../UIS44/README.md) へ遷移 |
| 3 | キャンセル・閉じる | ボタン押下 | 依頼せずに [UIS28](../UIS28/README.md) へ戻る |
| 4 | 展示のプレビュー・写真 | 項目押下 | [UIS28](../UIS28/README.md)（`exhibition_edit`）へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 対象のプレビュー | [UIS28](../UIS28/README.md)（`exhibition_edit`） | 画面へ遷移 |
| 全状態 | 画像 | [UIS28](../UIS28/README.md)（`exhibition_edit`） | 画面へ遷移 |
| 全状態 | PDFを作成する | [UIS44](../UIS44/README.md)（`export_pdf_processing`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| exhibition_id | 書き出す展示の ID | |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API75 | 本人の有料権限を取得する | なし |
| API64 | 展示を取得する | exhibition_id |

画面表示制御:

- 新しい PDF の書き出し依頼では、有料権限が有効な場合だけ表示する。有料権限がなければ [UIM08](../UIM08/README.md)、申し込みの確認中なら [UIS40](../UIS40/README.md) を表示する。失敗した依頼の再依頼は [UIS44](../UIS44/README.md#5-もう一度書き出す) から行う
- 「展示プラス」の印を付ける

### 2. PDF を作成する

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API78 | 展示の PDF の作成を依頼する | exhibition_id |

画面表示制御:

- 依頼を受け付けたら、[UIS44](../UIS44/README.md) へ遷移する。受け取った書き出しの ID を `export_id` として渡す
- 依頼時点の内容の保持と再依頼の区別は [共通仕様](../README.md#書き出しの失敗と再依頼) に従う。同じ内容の PDF を二重に作らない

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
