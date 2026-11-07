# [UIS30] 通知一覧

Figma で開く: [`notifications` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87394)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `notifications` | [4:87394](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87394) | [4:87507](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87507) | [4:87488](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87488) | [4:87611](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87611) |
| `notifications_empty` | [4:97529](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97529) | [4:97575](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97575) | [4:97560](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97560) | [4:97616](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-97616) |

## 概要

機能目的:

- 自分宛ての通知を見て、それぞれの対象へ移動してもらう

機能概要:

- 自分宛ての通知の一覧（すべて・未読・既読で絞り込み）
- 通知の対象の画面への移動と、既読にする処理
- 通知の設定への導線

関連する機能：F-01、F-02、F-03、F-04、F-05

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 自分宛ての通知を表示する |
| 2 | すべて・未読・既読 | タブ押下 | 同じ画面で通知を絞り込む |
| 3 | 通知 | 項目押下 | 通知を既読にし、対象の画面へ遷移 |
| 4 | 通知の設定へ | リンク押下 | [UIS33](../UIS33/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| `notifications` | そらさんがあなたをフォローしました。 | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| `notifications` | みなみさんがあなたの記録にコメントしました。 | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| `notifications` | そらさんが展示を公開しました。 | [UIS29](../UIS29/README.md)（`exhibition_detail`） | 画面へ遷移 |
| `notifications` | 迎えてから1年の記念日です。 | [UIS19](../UIS19/README.md)（`goods_detail`） | 画面へ遷移 |
| `notifications` | 記録の書き出しが完了しました。 | [UIS44](../UIS44/README.md)（`export_pdf_ready`） | 画面へ遷移 |
| `notifications` | 10月の月別ページができました。 | [UIS17](../UIS17/README.md)（`monthly`） | 画面へ遷移 |
| `notifications` | 金曜日の週末便（10月30日号）をお届けしました。 | [UIS09](../UIS09/README.md)（`home_following`） | 画面へ遷移 |
| `notifications` | 記録を見にいく | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| `notifications` | 展示を見る | [UIS29](../UIS29/README.md)（`exhibition_detail`） | 画面へ遷移 |
| `notifications` | 通知の設定へ | [UIS33](../UIS33/README.md)（`notification_settings`） | 画面へ遷移 |
| `notifications_empty` | みんなのよりみちを見る | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API73 | 自分宛ての通知を新しい順に取得する | 絞り込み（すべて・未読・既読）、ページ送りの位置 |

画面表示制御:

- 通知ごとに、文章・日時・未読かどうかを表示する
- 運営からのお知らせは、初版では表示しない（[ADR-0014](../../12_ADR/0014-管理画面を第2版へ移す.md)）
- 通知が 0 件の場合は「通知はまだありません。」と、ホームへの導線を表示する（`notifications_empty`）

### 3. 通知

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API74 | 通知を既読にする | 通知の ID |

画面表示制御：通知の種類ごとに、次の画面へ遷移する

| 通知の種類 | 遷移先 |
| --- | --- |
| フォローされた | [UIS23](../UIS23/README.md)（フォローした人のページ） |
| 記録へのいいね・コメント | [UIS14](../UIS14/README.md) |
| 展示へのいいね・コメント、フォローしている人の展示の公開 | [UIS29](../UIS29/README.md) |
| 好きなタグの週末便 | [UIS09](../UIS09/README.md)（`home_following`）。フォロー中には、フォローしているタグの記録も入る |
| お迎え記念日 | [UIS19](../UIS19/README.md) |
| 月別ページの完成 | [UIS17](../UIS17/README.md)（できた月）。毎月 1 日のバッチ（I-02）が作った後に、本人へ通知する |
| ストーリーズ用画像の完成 | [UIS43](../UIS43/README.md)（完成した状態） |
| PDF の完成 | [UIS44](../UIS44/README.md)（完成した状態） |

### 補足

通知は、サーバー側で通知用キューを通して作る。週末便は毎週金曜 19:00、お迎え記念日は毎朝 08:00（いずれも日本時間）のバッチが対象者を抽出する。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
