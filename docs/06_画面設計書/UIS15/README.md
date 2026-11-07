# [UIS15] わたしの記録（日付順）

Figma で開く: [`diary` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83580)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `diary` | [4:83580](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83580) | [4:83714](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83714) | [4:83681](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83681) | [4:83825](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-83825) |
| `diary_empty` | [4:96535](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96535) | [4:96621](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96621) | [4:96599](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96599) | [4:96695](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-96695) |

## 概要

機能目的:

- 自分の記録を、公開・非公開をまとめて日付順に見返してもらう

機能概要:

- 本人の記録を日付順に表示する（月ごと）
- カレンダー表示への切り替え
- 記録の詳細・編集・作成への導線

関連する機能：B-01、B-02

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 今月の本人の記録を表示する |
| 2 | 前の月・次の月 | ボタン押下 | 同じ画面で表示する月を切り替える |
| 3 | カレンダー | タブ押下 | [UIS16](../UIS16/README.md) へ遷移 |
| 4 | 記録 | 項目押下 | [UIS14](../UIS14/README.md) へ遷移 |
| 5 | 記録する | ボタン押下 | [UIS11](../UIS11/README.md) へ遷移 |
| 6 | 下書き | リンク押下 | [UIS13](../UIS13/README.md) へ遷移 |
| 7 | わたしのグッズ | リンク押下 | [UIS18](../UIS18/README.md) へ遷移 |
| 8 | 投稿者の名前・アイコン | 項目押下 | [UIS23](../UIS23/README.md)（`user_posts`）へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| `diary` | カレンダー | [UIS16](../UIS16/README.md)（`calendar`） | 画面へ遷移 |
| 全状態 | 下書き | [UIS13](../UIS13/README.md)（`drafts`） | 画面へ遷移 |
| 全状態 | わたしのグッズ | [UIS18](../UIS18/README.md)（`goods_list`） | 画面へ遷移 |
| `diary` | 記録の写真 | [UIS14](../UIS14/README.md)（`own_post_detail`） | 画面へ遷移 |
| `diary` | 記録のひとこと | [UIS14](../UIS14/README.md)（`own_post_detail`） | 画面へ遷移 |
| `diary` | 投稿者のアイコン | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| `diary` | 投稿者名 | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| `diary` | 記録する | [UIS11](../UIS11/README.md)（`post_create_photo`） | 画面へ遷移 |
| `diary_empty` | カレンダー | [UIS16](../UIS16/README.md)（`calendar_day_empty`） | 画面へ遷移 |
| `diary_empty` | 最初の記録を残す | [UIS11](../UIS11/README.md)（`post_create_photo`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| month | 表示する月 | 省略したら今月 |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API32 | 本人の記録を月ごとに取得する | month |

画面表示制御:

- 日付の縦線に沿って、日ごとに写真の記録と文字の記録を並べる
- 記録ごとに「公開」「自分だけ」の印を付ける
- 記録が 0 件の場合は「まだ記録がありません。」と、記録の作成への導線を表示する（`diary_empty`）

### 4. 記録

[UIS14](../UIS14/README.md) へ遷移する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 押した記録の ID | |

## 未確定事項

- 一覧から直接編集するボタンは Figma にない。編集は記録の詳細から開く。

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
