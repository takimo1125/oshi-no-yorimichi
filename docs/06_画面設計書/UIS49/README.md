# [UIS49] ページが見つかりません

Figma で開く: [`error_404` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91789)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `error_404` | [4:91789](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91789) | [4:91828](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91828) | [4:91817](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91817) | [4:91850](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-91850) |

## 概要

機能目的:

- 開こうとしたページがないことを伝え、ほかの画面へ戻ってもらう

機能概要:

- ページがないことの表示
- ホーム・前のページへの導線

関連する機能：なし

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | |
| 2 | ホームへ戻る | ボタン押下 | [UIS09](../UIS09/README.md) へ遷移 |
| 3 | 前のページへ | ボタン押下 | [UIS09](../UIS09/README.md)（`home`）へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | ホームへ戻る | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |
| 全状態 | 前のページへ | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ：なし

利用API：なし

画面表示制御:

- 「URL が変更されたか、ページが削除された可能性があります。」を表示する
- エラーの番号（404）は画面に出さない

### 2. ホームへ戻る

[UIS09](../UIS09/README.md) へ遷移する。未ログインの場合も同じ。

### 3. 前のページへ

Figma のリンクは [UIS09](../UIS09/README.md)（`home`）を示す。ブラウザーの履歴を戻す処理にはしない。

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
