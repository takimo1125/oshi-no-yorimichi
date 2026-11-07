# [UIM14] ログイン方法の解除の確認

Figma で開く: [`auth_method_remove_confirm` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11710)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `auth_method_remove_confirm` | [55:11710](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11710) | [55:11899](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11899) | [55:11741](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11741) | [55:11930](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11930) |

## 概要

機能目的:

- ログイン方法を解除する直前に、本当に解除するかを確かめる

機能概要:

- 解除するログイン方法と、解除した後に残る方法の表示
- ログイン方法の解除

関連する機能：A-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 解除するログイン方法を表示する |
| 2 | 解除する | ボタン押下 | ログイン方法を解除し、[UIS54](../UIS54/README.md) に戻る |
| 3 | キャンセル・閉じる | ボタン押下 | 何もせずにモーダルを閉じる |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 解除する | [UIS54](../UIS54/README.md)（`auth_methods`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| provider | `google` または `email` | 解除するログイン方法 |

利用API：なし（呼び出し元の [UIS54](../UIS54/README.md) が取得したログイン方法を使う）

画面表示制御:

- 見出しに、解除するログイン方法を示す（例：「Google でのログインを解除しますか？」）
- 解除しても記録・展示・契約はそのまま残ることと、解除した後に使うログイン方法を示す
- Figma は Google を解除する例。メールアドレスとパスワードを解除するときも同じ形にする

### 2. 解除する

[UIS54 の解除の条件](../UIS54/README.md#3-解除する) に従う。直近 10 分以内にログインしていない場合は、先に [UIS05](../UIS05/README.md)（`login_required`）でログインし直してもらう。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API16 | 認証方式の結び付きを解除する | provider |

画面表示制御:

- 解除に成功したら、モーダルを閉じて [UIS54](../UIS54/README.md) を表示し直す

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
