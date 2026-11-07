# [UIS21] グッズ情報の編集

Figma で開く: [`goods_edit` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84788)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `goods_edit` | [4:84788](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84788) | [4:84858](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84858) | [4:84837](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84837) | [4:84917](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84917) |

## 概要

機能目的:

- 登録済みのグッズの情報を直してもらう

機能概要:

- 写真・名前・お迎え日・公式ページの URL の変更

関連する機能：B-04

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 保存済みのグッズの情報を表示する |
| 2 | 変更を保存 | ボタン押下 | 変更を保存し、[UIS19](../UIS19/README.md) へ遷移 |
| 3 | キャンセル | ボタン押下 | 保存せずに [UIS19](../UIS19/README.md) へ遷移 |
| 4 | 写真を変更する | ボタン押下 | 新しい写真を選び、保存時に差し替える |
| 5 | このグッズを削除する | ボタン押下 | [UIM11](../UIM11/README.md) を起動し、確認したうえでグッズを削除して [UIS18](../UIS18/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 変更を保存 | [UIS19](../UIS19/README.md)（`goods_detail`） | 画面へ遷移 |
| 全状態 | キャンセル | [UIS19](../UIS19/README.md)（`goods_detail`） | 画面へ遷移 |
| 全状態 | このグッズを削除する | [UIM11](../UIM11/README.md)（`goods_delete_confirm`） | モーダルを起動 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| goods_id | 編集するグッズの ID | |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API42 | グッズを取得する | goods_id |

画面表示制御:

- 本人のグッズでない場合は編集させない

### 2. 変更を保存

入力チェック：[UIS20](../UIS20/README.md) のイベント 3 と同じ

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API44 | グッズを更新する | goods_id、入力フォームの値、画像 ID |

画面表示制御:

- 更新に成功したら [UIS19](../UIS19/README.md) へ遷移する

### 4. 写真を変更する

アップロードの処理は [UIS20](../UIS20/README.md) のイベント 2 と同じ。新しい写真は、イベント 2 の保存で差し替える。

### 5. このグッズを削除する

[UIM11](../UIM11/README.md) で確認してから削除する。

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API45 | グッズを削除する | goods_id |

画面表示制御:

- グッズを削除しても、記録は残す。記録とグッズの結び付きだけを外す
- 削除に成功したら [UIS18](../UIS18/README.md) へ遷移する

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
