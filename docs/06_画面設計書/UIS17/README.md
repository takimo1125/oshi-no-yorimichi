# [UIS17] 月別ページ

Figma で開く: [`monthly` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87218)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `monthly` | [4:87218](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87218) | [4:87301](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87301) | [4:87285](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87285) | [4:87378](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87378) |
| `monthly_not_ready` | [49:8626](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-8626) | [49:8715](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-8715) | [49:8693](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-8693) | [49:8792](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-8792) |

## 概要

機能目的:

- 前の月の自分の写真を日付順に並べたページで、月ごとに振り返ってもらう

機能概要:

- 月ごとの写真のページの表示（本人だけが見られる）
- 表示する月の切り替え
- 元の記録への導線

関連する機能：C-06、I-02

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 指定した月のページを表示する |
| 2 | 月を選ぶ | タブ押下 | 同じ画面で別の月のページに切り替える |
| 3 | 記録を見る | 項目押下 | [UIS14](../UIS14/README.md) へ遷移 |
| 4 | わたしの記録へ | リンク押下 | [UIS15](../UIS15/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 記録の項目 | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| 全状態 | 画像 | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| 全状態 | 記録を見る | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| 全状態 | わたしの記録へ | [UIS15](../UIS15/README.md)（`diary`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| month | 表示する月 | 省略したら、作成済みのいちばん新しい月 |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API40 | 本人の月別ページを取得する | month |

画面表示制御:

- 月別ページは、毎月 1 日のバッチが前の月の分を作る。画面では作らない
- 「自分のみ」の印を付ける。初版では本人だけが見られる。ほかの利用者・未ログインには公開せず、公開する操作も作らない
- 入口は、[UIS16](../UIS16/README.md) の月の見出しと、月別ページの完成通知（[UIS30](../UIS30/README.md)）。完成通知は [UIS30](../UIS30/README.md) の通知一覧に描いている。カレンダーの月の見出しは、Figma の例が月別ページのまだない月（2026年11月）のため、リンクを設定していない
- 指定した月のページがまだない場合は、「この月のページはまだできていません」と表示する（`monthly_not_ready`）

### 3. 記録を見る

[UIS14](../UIS14/README.md) へ遷移する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 押した写真の元の記録の ID | |

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
