# [UIS12] 記録の編集

Figma で開く: [`post_edit` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-82886)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `post_edit` | [4:82886](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-82886) | [4:83005](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83005) | [4:82977](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-82977) | [4:83106](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83106) |
| `post_edit_text` | [4:95511](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-95511) | [4:95606](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-95606) | [4:95586](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-95586) | [4:95691](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-95691) |

## 概要

機能目的:

- 投稿した後の自分の記録を直してもらう

機能概要:

- 写真・ひとこと・記録の種類・タグ・登場したグッズ・公開範囲の変更
- 記録の削除への導線

関連する機能：B-06

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 保存済みの記録の内容を表示する |
| 2 | 写真を追加 | ボタン押下 | [UIS11](../UIS11/README.md) のイベント 2 と同じ |
| 3 | 写真の削除アイコン | ボタン押下 | 選んだ写真を記録から外す |
| 4 | 登場したグッズ | 入力欄押下 | [UIM02](../UIM02/README.md) を起動 |
| 5 | 変更を保存 | ボタン押下 | 変更を保存し、[UIS14](../UIS14/README.md) へ遷移 |
| 6 | キャンセル | ボタン押下 | 写真の編集は [UIS15](../UIS15/README.md)、文字の編集は [UIS14](../UIS14/README.md)（`own_post_detail_text`）へ遷移 |
| 7 | この記録を削除 | リンク押下 | [UIM03](../UIM03/README.md) を起動 |
| 8 | タグを追加 | ボタン押下 | [UIS24](../UIS24/README.md)（タグ検索）へ遷移し、選んだタグを入力欄に足して戻る |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | タグを追加 | [UIS24](../UIS24/README.md)（`search_tags`） | 画面へ遷移 |
| `post_edit` | 登場したグッズ | [UIM02](../UIM02/README.md)（`goods_picker`） | モーダルを起動 |
| 全状態 | 公開 | 同じ画面で選択した値を表示 | 選択状態の変更 |
| `post_edit` | 変更を保存 | [UIS14](../UIS14/README.md)（`own_post_detail_updated`） | 画面へ遷移 |
| `post_edit` | キャンセル | [UIS15](../UIS15/README.md)（`diary`） | 画面へ遷移 |
| 全状態 | この記録を削除 | [UIM03](../UIM03/README.md)（`post_delete_confirm`） | モーダルを起動 |
| `post_edit_text` | 変更を保存 | [UIS14](../UIS14/README.md)（`own_post_detail_text`） | 画面へ遷移 |
| `post_edit_text` | キャンセル | [UIS14](../UIS14/README.md)（`own_post_detail_text`） | 画面へ遷移 |

上表は Figma の表示例の配線を示す。保存後に表示する公開範囲・写真の有無・保存完了表示はイベント 5 に従い、表示例の非公開状態で更新結果を上書きしない。

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 編集する記録の ID | |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API30 | 記録を取得する | post_id |

画面表示制御:

- 本人の記録でない場合は編集させない。表示は [UIS49](../UIS49/README.md) とするか未確定
- 写真がない記録は、文字だけの記録の表示にする（`post_edit_text`）
- 公開範囲には、保存済みの値を選んだ状態で表示する

### 5. 変更を保存

入力チェック：[UIS11](../UIS11/README.md) のイベント 8 と同じ

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API29 | 記録を更新する | post_id、入力フォームの値、画像 ID |

画面表示制御:

- 更新に成功したら [UIS14](../UIS14/README.md) へ遷移する。保存した記録の公開範囲と写真の有無に合った表示を選び、写真・文字、公開・非公開のどの組み合わせでも保存完了を知らせる
- 表示の切り替えと保存完了の文言は [UIS14 の画面表示制御](../UIS14/README.md#1-初期表示) に従う
- 保存結果を確認できない場合は [共通仕様](../README.md#保存の結果を確認できないとき) に従い、この画面に入力を保持する

起動パラメータ（遷移先へ渡す）:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 編集した記録の ID | |
| saved | `true` | 写真・文字、公開・非公開を問わず、更新に成功した直後に渡す |

### 6. キャンセル

[共通の離脱確認](../README.md#未保存の入力と離脱) に従う。変更がある場合は確認し、破棄して移動することを選んだら保存せずに戻る。`post_edit` のリンクは [UIS15](../UIS15/README.md)、`post_edit_text` のリンクは [UIS14](../UIS14/README.md) の `own_post_detail_text` を示す。

### 7. この記録を削除

[UIM03](../UIM03/README.md) を起動する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 編集中の記録の ID | |

## 未確定事項

- 写真なしの編集モデルにグッズ選択の入口は描かれていない。タグを選んだ後の戻り方は [UIS11](../UIS11/README.md#4-タグを追加) と同じ
