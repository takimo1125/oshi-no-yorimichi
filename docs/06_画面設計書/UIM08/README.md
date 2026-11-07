# [UIM08] 展示プラスの案内

Figma で開く: [`plus_gate_pdf` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99936)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `plus_gate_pdf` | [4:99936](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99936) | [4:99985](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99985) | [4:99969](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-99969) | [4:100018](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100018) |
| `plus_gate_multiple` | [4:100034](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100034) | [4:100083](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100083) | [4:100067](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100067) | [4:100116](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-100116) |

## 概要

機能目的:

- 有料権限のない人が展示プラスの機能を使おうとしたときに、展示プラスで使えることを案内する

機能概要:

- 使おうとした機能（PDF の書き出し・複数の展示）が展示プラスの機能であることの表示
- 展示プラスの案内への導線

関連する機能：E-06、E-07、G-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 使おうとした機能に合わせた案内を表示する |
| 2 | 展示プラスの内容を見る | ボタン押下 | [UIS38](../UIS38/README.md) へ遷移 |
| 3 | 展示に戻る・わたしの展示へ戻る | ボタン押下 | 呼び出し元へ戻る |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 展示プラスの内容を見る | [UIS38](../UIS38/README.md)（`plus_inactive`） | 画面へ遷移 |
| `plus_gate_pdf` | 展示に戻る | [UIS28](../UIS28/README.md)（`exhibition_edit`） | 画面へ遷移 |
| `plus_gate_multiple` | わたしの展示へ戻る | [UIS25](../UIS25/README.md)（`exhibitions`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| feature | `pdf_export` または `multiple_exhibitions` | 使おうとした機能 |

画面表示制御:

| feature | 表示 | 画面モデル |
| --- | --- | --- |
| `pdf_export` | 「展示の PDF 書き出しは、展示プラスでご利用いただけます。」と料金 | `plus_gate_pdf` |
| `multiple_exhibitions` | 「複数の展示づくりは、展示プラスでご利用いただけます。」と料金 | `plus_gate_multiple` |

- 無料で保持できる展示数は [UIS25](../UIS25/README.md#展示数と契約終了後の操作)、料金と利用権は [契約条件](../UIS38/README.md#展示プラスの契約条件) に従う。現行 Figma に無料 1 展示の案内は未反映。保存期限は未確定のため追加しない

### 3. 戻る

`pdf_export` のときは [UIS28](../UIS28/README.md)、`multiple_exhibitions` のときは [UIS25](../UIS25/README.md) へ戻る。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
