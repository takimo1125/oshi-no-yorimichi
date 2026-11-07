# [UIS45] 通報

Figma で開く: [`report_form` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89784)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `report_form` | [4:89784](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89784) | [4:89868](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89868) | [4:89853](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89853) | [4:89947](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89947) |
| `report_sent` | [4:89962](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-89962) | [4:90013](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-90013) | [4:90002](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-90002) | [4:90044](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-90044) |

## 概要

機能目的:

- 問題のある記録・コメント・展示・利用者を運営に知らせてもらう

機能概要:

- 通報の対象の表示
- 通報の理由と詳しい内容の入力
- 受け付けたことの表示

関連する機能：H-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 通報の対象を表示する |
| 2 | 通報する | ボタン押下 | 通報を送り、受け付けたことの表示に切り替える |
| 3 | キャンセル・この記録にもどる | ボタン押下 | Figma の表示例は [UIS14](../UIS14/README.md)（`post_detail`）へ遷移 |
| 4 | みんなのよりみちにもどる | ボタン押下 | [UIS09](../UIS09/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 対象のプレビュー | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| 全状態 | 画像 | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| `report_form` | 通報する | 同じ画面（`report_sent`） | 状態の切り替え |
| `report_form` | キャンセル | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| `report_sent` | この記録にもどる | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| `report_sent` | みんなのよりみちにもどる | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| target_type | `post`・`comment`・`exhibition`・`user` のどれか | |
| target_id | 対象の ID | |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API81 | 通報の対象を取得する | target_type、target_id |

画面表示制御:

- 対象の種類に合わせて、説明の文言を変える（例：「この投稿について」）

### 2. 通報する

入力チェック:

| 項目 | チェック |
| --- | --- |
| 通報の理由 | 「不適切と感じる内容」「迷惑な内容」「個人情報が含まれる」「その他」から選ぶ。1 つだけ選ぶ |
| 詳しい内容 | 任意。500 文字まで |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API82 | 通報を登録する | target_type、target_id、理由、詳しい内容 |

画面表示制御:

- 登録に成功したら、受け付けたことの表示に切り替える（`report_sent`）。送る前には受け付けたと表示しない
- 対応の結果や期限は約束しない

### 3. キャンセル・この記録にもどる

Figma の表示例は記録を対象にしており、キャンセル・受付完了後の戻る操作は [UIS14](../UIS14/README.md)（`post_detail`）へ進む。展示・コメント・利用者を対象にした場合の戻り先の切り替えは未確定。`target_type` と `target_id` は保持する。

### 補足

初版には管理画面がないため、通報が届いたら Slack に知らせ、運営者が管理者用のコマンドで対応する（[ADR-0014](../../12_ADR/0014-管理画面を第2版へ移す.md)）。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
