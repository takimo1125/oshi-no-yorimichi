# [UIS54] ログイン方法

Figma で開く: [`auth_methods` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11224)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `auth_methods` | [49:11224](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11224) | [49:11315](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11315) | [49:11282](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11282) | [49:11383](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-11383) |
| `auth_methods_google_linked` | [55:11762](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11762) | [55:11951](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11951) | [55:11810](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11810) | [55:12009](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-12009) |
| `auth_methods_error` | [55:11829](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11829) | [55:12028](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-12028) | [55:11882](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-11882) | [55:12091](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=55-12091) |

## 概要

機能目的:

- ログインに使う方法（メールアドレスとパスワード・Google）を確かめ、追加・解除してもらう

機能概要:

- ログイン方法の一覧と、それぞれの状態の表示
- Google の追加
- ログイン方法の解除

関連する機能：A-01

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 本人のログイン方法を表示する |
| 2 | Google を追加する | ボタン押下 | Google の認証を経て、同じ利用者に結び付ける |
| 3 | 解除する | ボタン押下 | [UIM14](../UIM14/README.md) で確認したうえで、利用できる方法を最低 1 つ残して解除する |
| 4 | 設定へ戻る | ボタン押下 | [UIS31](../UIS31/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 設定へ戻る | [UIS31](../UIS31/README.md)（`settings`） | 画面へ遷移 |
| `auth_methods_google_linked` | 解除する（Google） | [UIM14](../UIM14/README.md)（`auth_method_remove_confirm`） | モーダルを起動 |

### 1. 初期表示

起動パラメータ：なし

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API15 | 本人の認証方式を取得する | なし |

画面表示制御:

- 「メールアドレスとパスワード」と「Google」を並べ、それぞれの状態（メールアドレス・連携していないこと）を表示する
- 連携していない方法には「追加する」、連携している方法には「解除する」を置く
- 解除すると使えるログイン方法が残らない場合は、「解除する」を押せなくし、「最後の 1 つなので解除できません」と理由を添える
- Google で登録した人もパスワードを持つ（[ADR-0027](../../12_ADR/0027-Googleで登録するときもパスワードを決めてもらう.md)）。Figma の `auth_methods` はメールアドレスとパスワードだけを使っている例、`auth_methods_google_linked` は両方を使っている例

### 2. Google を追加する

現在利用している認証方式で改めて本人確認し、その後、追加する方式でも認証する。直近 10 分以内にログインしていない場合は、先に [UIS05](../UIS05/README.md)（`login_required`）でログインし直してもらう（API が `403 reauthentication_required` を返す）。両方の確認が成功してから、[ADR-0026](../../12_ADR/0026-確認済みのメールアドレスが一致したら認証方式を自動で結び付ける.md) に従って連携する。確認途中や失敗時には、連携済みとして扱わない。

すでに別々の利用者として登録されている場合、その利用者同士の統合は提供しない。別の利用者に結び付いている認証方式を追加する操作で、記録・展示・契約を統合したり、結び付きを移し替えたりしない。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API06 | Google の認証を始める（連携） | `mode=link` |

画面表示制御:

- Google の認証から戻ったら、この画面を表示し直す
- 追加に失敗した・中断した場合は、「Google を追加できませんでした。もう一度お試しください。」を表示する（`auth_methods_error`）。ほかの利用者に結び付いている Google アカウントの場合も同じ表示にし、別の人が使っていることを画面から読み取れないようにする

### 3. 解除する

解除後も利用できるログイン方式が最低 1 つ残る場合に限り解除できる。最後の 1 つは解除できない。サーバー側でもこの条件を確かめる。認証方式の解除は、利用者の退会や記録・展示・契約の削除として扱わない。解除の前にも、直近 10 分以内のログインを求める。解除する前に、[UIM14](../UIM14/README.md) で確認する。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API16 | 認証方式の結び付きを解除する | provider |

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
