# [UIS29] 展示の詳細

Figma で開く: [`exhibition_detail` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-86960)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `exhibition_detail` | [4:86960](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-86960) | [4:87084](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87084) | [4:87061](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87061) | [4:87195](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-87195) |
| `exhibition_preview` | [49:9970](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-9970) | [49:10100](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10100) | [49:10071](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10071) | [49:10211](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10211) |

## 概要

機能目的:

- 公開されたテーマ展示を見てもらい、いいね・コメント・共有で反応してもらう

機能概要:

- 展示の表紙・タイトル・説明と、並べた記録と解説の表示
- いいね・コメント・共有
- 通報への導線
- 所有者のプレビュー

関連する機能：D-01、D-04、E-02、E-05、H-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 展示を表示する |
| 2 | いいね | ボタン押下 | いいねの状態を切り替える |
| 3 | 共有 | ボタン押下 | 展示の URL を共有する |
| 4 | コメントする | ボタン押下 | コメントを送る |
| 5 | 作者 | 項目押下 | [UIS23](../UIS23/README.md) へ遷移 |
| 6 | 通報 | リンク押下 | [UIS45](../UIS45/README.md) へ遷移 |
| 7 | みんなの展示にもどる | リンク押下 | [UIS51](../UIS51/README.md) へ遷移 |
| 8 | 編集に戻る | 操作実行 | プレビューから入力を保持して [UIS28](../UIS28/README.md) へ戻る |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | プロフィール欄 | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| 全状態 | 通報 | [UIS45](../UIS45/README.md)（`report_form`） | 画面へ遷移 |
| `exhibition_detail` | みんなの展示にもどる | [UIS51](../UIS51/README.md)（`public_exhibitions`） | 画面へ遷移 |
| `exhibition_preview` | 編集に戻る | [UIS28](../UIS28/README.md)（`exhibition_edit`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| exhibition_id | 表示する展示の ID | 通常閲覧では保存済みの展示の ID。プレビューでは作成中の ID（保存前でもよい） |
| preview | `true` | [UIS28](../UIS28/README.md) から所有者のプレビューとして開くときだけ渡す。入力中の内容は sessionStorage から読み、API64・API67 は呼ばない。記録の写真などを読み直すときは API32（`ids` の指定）を使う（[API 設計書の「画面間の入力の受け渡し」](../../07_API設計書/README.md#画面間の入力の受け渡し)） |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API64 | 展示を取得する | exhibition_id |
| API67 | 展示へのコメントを取得する | exhibition_id |

画面表示制御:

- 他の利用者の公開された展示の場合は、いいね・共有・コメント・通報を表示する。所有者向けの編集の操作は出さない
- [UIS28](../UIS28/README.md) の「プレビューで確認」は `exhibition_preview`、[UIS25](../UIS25/README.md) の「見る」は `exhibition_detail` へ進む。Figma のモデルは他者の公開展示で、通報・共有・コメントを表示する。編集中のプレビューとは表示条件を分ける
- `preview=true` の場合は [UIS28 のプレビュー仕様](../UIS28/README.md#4-プレビューで確認) に従い、受け取った入力中の内容を表示する。保存・公開の処理は行わず、新規展示のプレビューに保存済み展示の ID を必須としない。通常閲覧用の展示取得で入力中の内容を上書きしない
- 編集中のプレビュー（`exhibition_preview`）では、「プレビューです。まだ保存していません。」と表示し、いいね・共有・コメント・通報の表示と操作を出さず、コメント取得も行わない。「編集に戻る」を表示する。これらの操作は通常閲覧に対してのみ行う
- 他の利用者の非公開の展示・存在しない展示の場合は、[UIS49](../UIS49/README.md) を表示する
- SNS に URL を貼ったときのカード画像（OGP）を、展示ごとに設定する（E-05）

### 2. いいね

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API69・API70 | 展示にいいねする、またはいいねを取り消す | exhibition_id |

### 3. 共有

この展示の URL を共有する。端末の共有機能を使うか、URL をコピーするかは未確定。

### 4. コメントする

入力チェック:

| 項目 | チェック |
| --- | --- |
| コメント | 必須。300 文字まで |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API68 | 展示にコメントを投稿する | exhibition_id、コメント |

画面表示制御:

- 投稿に成功したら、コメントの一覧を取得し直す

### 6. 通報

[UIS45](../UIS45/README.md) へ遷移する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| target_type | `exhibition` | |
| target_id | exhibition_id | |

### 8. 編集に戻る

編集中のプレビューから [UIS28](../UIS28/README.md) へ戻る。[共通の入力保持](../README.md#未保存の入力と離脱) に従い、プレビュー前の入力内容を保って編集を続ける。

## 未確定事項

- [UIS25](../UIS25/README.md) の「見る」から開いた本人展示の表示・戻り先は未確定
