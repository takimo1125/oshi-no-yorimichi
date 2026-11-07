# [UIS44] PDF 書き出しの状況

Figma で開く: [`export_pdf_processing` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89538)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `export_pdf_processing` | [4:89538](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89538) | [4:89609](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89609) | [4:89594](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89594) | [4:89656](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89656) |
| `export_pdf_ready` | [4:89671](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89671) | [4:89732](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89732) | [4:89719](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89719) | [4:89771](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89771) |
| `export_pdf_failed` | [49:11013](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11013) | [49:11153](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11153) | [49:11070](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11070) | [49:11201](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11201) |

## 概要

機能目的:

- 展示プラスの契約者に、展示の PDF の作成の状況を伝え、完成した PDF を保存してもらう

機能概要:

- 作成中の表示
- 完成した PDF の端末への保存
- 作成に失敗した状態の表示と再依頼

関連する機能：E-06、F-05

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | PDF の作成の状態に合わせた表示にする |
| 2 | PDF を保存 | ボタン押下 | 完成した PDF を端末に保存する |
| 3 | 通知を見る | リンク押下 | [UIS30](../UIS30/README.md) へ遷移 |
| 4 | 展示に戻る | ボタン押下 | [UIS28](../UIS28/README.md) へ遷移 |
| 5 | もう一度書き出す | 操作実行 | 失敗した PDF の書き出しを再依頼する |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 展示に戻る | [UIS28](../UIS28/README.md)（`exhibition_edit`） | 画面へ遷移 |
| `export_pdf_failed` | もう一度書き出す | 同じ画面（`export_pdf_processing`） | 状態の切り替え |
| `export_pdf_processing` | 通知を見る | [UIS30](../UIS30/README.md)（`notifications`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| export_id | 書き出しの ID | [UIM07](../UIM07/README.md) の依頼受付後、状態確認・失敗後の再依頼・完成の通知から開く場合に使用する |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API79 | 書き出しの状態を取得する | export_id |

画面表示制御:

| 状態 | 表示 | 画面モデル |
| --- | --- | --- |
| 作成中 | 「PDF を作成しています」・収録する記録の一覧・「通知を見る」 | `export_pdf_processing` |
| 完成 | PDF のプレビュー・「PDF を保存」 | `export_pdf_ready` |
| 失敗 | 「PDFを作成できませんでした」・元の展示は残っていること・契約が終わった後でも書き出せること・「もう一度書き出す」。対象の展示を削除した後は「対象が削除されたため、書き出せません」とし、「もう一度書き出す」を出さない（[共通の失敗表示と再依頼](../README.md#書き出しの失敗と再依頼)） | `export_pdf_failed` |

- 作成中の表示には、保存のボタン・進み具合の割合・かかる時間を出さない
- 有料権限を確かめたうえで依頼された書き出しだけを表示する。無料の利用者の表示と混ぜない

### 2. PDF を保存

完成した PDF ファイルを端末に保存する。追加の料金・保存の期限・ファイルの大きさは表示しない（決まっていないため）。

### 5. もう一度書き出す

失敗した書き出しに対し、契約終了後の扱いを含めて [共通の再依頼処理](../README.md#書き出しの失敗と再依頼) を行う。

### 補足

PDF は、書き出し用キューを通して ECS のワーカーが作る。完成したら通知用キューを通して通知が届く（E-06・F-05）。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
