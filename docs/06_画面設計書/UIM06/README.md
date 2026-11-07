# [UIM06] ミュートの確認

Figma で開く: [`mute_confirm` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91713)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `mute_confirm` | [4:91713](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91713) | [4:91751](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91751) | [4:91740](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91740) | [4:91778](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91778) |

## 概要

機能目的:

- 他の利用者をミュートする直前に、本当にミュートするかを確かめる

機能概要:

- 対象の利用者の表示
- ミュートの実行

関連する機能：D-03

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 対象の利用者を表示する |
| 2 | ミュートする | ボタン押下 | ミュートし、[UIS23](../UIS23/README.md)（`user_posts`）へ遷移 |
| 3 | キャンセル | ボタン押下 | 何もせずにモーダルを閉じる |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | ミュートする | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| user_name | 対象の利用者のユーザー名 | |

### 2. ミュートする

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API59 | 利用者をミュートする | user_name |

画面表示制御:

- ミュートに成功したら、モーダルを閉じて [UIS23](../UIS23/README.md) に戻る

### ミュートの効果

- ミュートした人のホーム（[UIS09](../UIS09/README.md)）・タグのページ（[UIS22](../UIS22/README.md)）・週刊ギャラリー（[UIS10](../UIS10/README.md)）から、相手の記録を外す。相手からの通知も止める
- 相手には知らせない。相手からは、これまでどおり自分の記録が見える
- 相手のプロフィールを直接開けば、相手の記録を見られる
- 解除は、相手のプロフィール（[UIS23](../UIS23/README.md)）と、ブロック・ミュートした人の一覧（[UIS53](../UIS53/README.md)）で行う

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
