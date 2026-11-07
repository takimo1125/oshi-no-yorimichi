# [UIM02] グッズを選ぶ

Figma で開く: [`goods_picker` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91399)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `goods_picker` | [4:91399](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91399) | [4:91454](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91454) | [4:91440](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91440) | [4:91495](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91495) |

## 概要

機能目的:

- 記録に写っているグッズを、登録済みのグッズから選んでもらう

機能概要:

- 本人の登録済みグッズの一覧と検索
- グッズの選択
- グッズの登録への導線

関連する機能：B-05

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 本人のグッズを表示する |
| 2 | グッズを検索 | 入力欄押下 | [UIS24](../UIS24/README.md)（`search_tags`）へ遷移 |
| 3 | グッズ | 項目押下 | 選択と選択の解除を切り替える |
| 4 | 選択したグッズを追加 | ボタン押下 | [UIS11](../UIS11/README.md)（`post_create_photo`）へ遷移 |
| 5 | キャンセル・× | ボタン押下 | 何も返さずにモーダルを閉じる |
| 6 | 新しいグッズを登録 | リンク押下 | [UIS20](../UIS20/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | グッズを検索 | [UIS24](../UIS24/README.md)（`search_tags`） | 画面へ遷移 |
| 全状態 | 選択したグッズを追加 | [UIS11](../UIS11/README.md)（`post_create_photo`） | 画面へ遷移 |
| 全状態 | 新しいグッズを登録 | [UIS20](../UIS20/README.md)（`goods_create`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| selected_goods_ids | 呼び出し元でいま選んでいるグッズの ID | 選択済みの状態で表示する |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API41 | 本人のグッズを取得する | なし |

画面表示制御:

- PC では画面の中央のダイアログ、スマホでは下からのシートで表示する

### 2. グッズを検索

Figma の入力欄のリンクは [UIS24](../UIS24/README.md)（`search_tags`）を示す。説明フレームにあるグッズの検索と、タグ検索への遷移が一致しない。グッズ名で絞り込む操作・検索結果の戻し方は未確定。

### 4. 選択したグッズを追加

選んだグッズの ID を渡し、Figma のリンクどおり [UIS11](../UIS11/README.md)（`post_create_photo`）へ遷移する。ここでは記録を保存しない。[UIS12](../UIS12/README.md) から開いた場合に編集画面へ戻す方法は未確定。

### 6. 新しいグッズを登録

[UIS20](../UIS20/README.md) へ遷移する。グッズの登録は、記録の必須の条件ではない。UIS20 を `return_to=<元の画面>` で開き、登録後は `picked_goods_id=<ID>` を付けて元の画面へ戻る。入力中の内容は sessionStorage から復元する（[API 設計書の「画面間の入力の受け渡し」](../../07_API設計書/README.md#画面間の入力の受け渡し)）。Figma の登録後のリンクは [UIS19](../UIS19/README.md) を示す。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
