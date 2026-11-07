# [UIS16] わたしの記録（カレンダー）

Figma で開く: [`calendar` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83858)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `calendar` | [4:83858](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83858) | [4:84079](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84079) | [4:84048](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84048) | [4:84279](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84279) |
| `calendar_day_empty` | [4:96717](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96717) | [4:96881](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96881) | [4:96860](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96860) | [4:97034](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97034) |

## 概要

機能目的:

- 自分の記録を月のカレンダーで見返してもらう

機能概要:

- 記録のある日に印を付けた月のカレンダー
- 選んだ日の記録の表示
- 記録の種類での絞り込み

関連する機能：B-08

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 今月のカレンダーと、今日の記録を表示する |
| 2 | 日付 | 項目押下 | 選んだ日の記録を表示する |
| 3 | 前の月・次の月 | ボタン押下 | 同じ画面で月を切り替える |
| 4 | 記録の種類 | タブ押下 | 選んだ種類の記録だけを表示する |
| 5 | 一覧で見る | タブ押下 | [UIS15](../UIS15/README.md) へ遷移 |
| 6 | 記録 | 項目押下 | [UIS12](../UIS12/README.md) へ遷移 |
| 7 | 記録する | ボタン押下 | [UIS11](../UIS11/README.md) へ遷移 |
| 8 | 下書き | リンク押下 | [UIS13](../UIS13/README.md) へ遷移 |
| 9 | わたしのグッズ | リンク押下 | [UIS18](../UIS18/README.md) へ遷移 |
| 10 | 投稿者の名前・アイコン | 項目押下 | [UIS23](../UIS23/README.md)（`user_posts`）へ遷移 |
| 11 | 月の見出し | 項目押下 | その月の月別ページ（[UIS17](../UIS17/README.md)）へ遷移。まだ作られていない月は押せない |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| `calendar` | 日付（2日） | 同じ画面（`calendar_day_empty`） | 状態の切り替え |
| `calendar`・`calendar_day_empty` | 一覧で見る | [UIS15](../UIS15/README.md)（`diary`） | 画面へ遷移 |
| 全状態 | 下書き | [UIS13](../UIS13/README.md)（`drafts`） | 画面へ遷移 |
| 全状態 | わたしのグッズ | [UIS18](../UIS18/README.md)（`goods_list`） | 画面へ遷移 |
| `calendar` | 記録の写真 | [UIS12](../UIS12/README.md)（`post_edit`） | 画面へ遷移 |
| `calendar` | 記録のひとこと | [UIS12](../UIS12/README.md)（`post_edit`） | 画面へ遷移 |
| `calendar` | 投稿者のアイコン | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| `calendar` | 投稿者名 | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| 全状態 | 記録する | [UIS11](../UIS11/README.md)（`post_create_photo`） | 画面へ遷移 |
| `calendar_day_empty` | 日付（1日） | 同じ画面（`calendar`） | 状態の切り替え |
| `calendar_day_empty` | 日付（3日） | 同じ画面（`calendar`） | 状態の切り替え |
| `calendar_day_empty` | 日付（4日） | 同じ画面（`calendar`） | 状態の切り替え |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| month | 表示する月 | 省略したら今月 |
| date | 選ぶ日 | 省略したら今日 |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API32 | 本人の記録を月ごとに取得する | month、記録の種類 |

画面表示制御:

- 記録のある日に印を付ける
- PC ではカレンダーを左、選んだ日の記録を右に置く。スマホでは選んだ日の記録をカレンダーの下に置く
- 予定を管理する機能は加えない

### 2. 日付

画面表示制御:

- 選んだ日の記録を表示する
- 選んだ日に記録がない場合は、その日だけを 0 件の表示にする（`calendar_day_empty`）。ほかの日の印はそのまま残す
- 記録がない日を選んだときも、記録がある日と同じ位置に「一覧で見る」を表示する。Figma は `calendar_day_empty` にも描いている

### 4. 記録の種類

「すべて」「飾った」「連れていった」「迎えた」「参戦した」から選ぶ。初期値は「すべて」。

### 6. 記録

[UIS12](../UIS12/README.md) へ遷移する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 押した記録の ID | |

## 未確定事項

- 月の見出しから月別ページへのリンクは、Figma の例（2026年11月）がまだ作られていない月のため、設定していない。記録のあるカレンダーから記録を開くリンクは [UIS12](../UIS12/README.md) を採用する
