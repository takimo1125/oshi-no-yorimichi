# [UIS37] 退会の受付完了

Figma で開く: [`withdraw_complete` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110262)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `withdraw_complete` | [19:110262](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110262) | [19:110298](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110298) | [19:110289](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110289) | [19:110319](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=19-110319) |

## 概要

機能目的:

- 退会を受け付けたことと、データを削除する時期を伝える

機能概要:

- 退会の受付の表示
- トップページへの導線

関連する機能：A-04

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | ホームへ戻る | ボタン押下 | [UIS01](../UIS01/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | ホームへ戻る | [UIS01](../UIS01/README.md)（`lp`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API：なし

画面表示制御:

- 未ログインのヘッダーを使う
- 削除時期は [UIS35 の期間の定義](../UIS35/README.md#退会の期間と公開停止) に従う。現行 Figma は「退会から 1 か月後にデータを削除します」の表示
- 現行 Figma にアカウントの編集や復元の導線はない。この画面にも取消しの導線は置かない。退会の取消しは、期間内に再びログインしたときに案内する（[UIS52](../UIS52/README.md)）

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
