# [UIS13] 下書き一覧

Figma で開く: [`drafts` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83134)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `drafts` | [4:83134](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83134) | [4:83210](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83210) | [4:83186](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83186) | [4:83272](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83272) |
| `drafts_empty` | [4:97055](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97055) | [4:97104](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97104) | [4:97088](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97088) | [4:97147](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97147) |

## 概要

機能目的:

- 途中で保存した記録を見つけ、続きを書いてもらう

機能概要:

- 本人の下書きの一覧（本人だけが見られる）
- 下書きの続きを書く。削除の操作は未確定事項に記す

関連する機能：B-06

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 本人の下書きを表示する |
| 2 | 下書き | 項目押下 | [UIS11](../UIS11/README.md) へ遷移し、続きを書く |
| 3 | 新しく記録する | ボタン押下 | [UIS11](../UIS11/README.md) へ遷移 |
| 4 | わたしの記録にもどる | リンク押下 | [UIS15](../UIS15/README.md) へ遷移 |
| 5 | 削除 | ボタン押下 | [UIM10](../UIM10/README.md) を起動し、確認したうえで下書きを削除する |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| `drafts` | 記録の項目 | [UIS11](../UIS11/README.md)（`post_create_photo`） | 画面へ遷移 |
| `drafts` | 記録の項目 | [UIS11](../UIS11/README.md)（`post_create_text`） | 画面へ遷移 |
| 全状態 | 新しく記録する | [UIS11](../UIS11/README.md)（`post_create_photo`） | 画面へ遷移 |
| 全状態 | わたしの記録にもどる | [UIS15](../UIS15/README.md)（`diary`） | 画面へ遷移 |
| `drafts` | 削除 | [UIM10](../UIM10/README.md)（`draft_delete_confirm`） | モーダルを起動 |

### 1. 初期表示

起動パラメータ：なし

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API25 | 本人の下書きを取得する | ページ送りの位置 |

画面表示制御:

- 下書きを日付ごとにまとめ、タイトル・本文の書き出し・最終保存の日時を表示する
- 下書きが 0 件の場合は、0 件の表示と、記録の作成への導線を表示する（`drafts_empty`）

### 2. 下書き

[UIS11](../UIS11/README.md) へ遷移する。写真のある下書きは写真のある記録の表示、文字だけの下書きは文字だけの記録の表示で開く。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| draft_id | 押した下書きの ID | |

### 5. 削除

一覧の各下書きに「削除」を置き、[UIM10](../UIM10/README.md) で確認してから削除する。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API28 | 下書きを削除する | draft_id |

画面表示制御:

- 削除に成功したら、同じ一覧を表示し直す。下書きが 0 件になった場合は 0 件の表示にする（`drafts_empty`）

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
