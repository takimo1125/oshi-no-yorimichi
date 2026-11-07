# [UIS19] グッズの詳細

Figma で開く: [`goods_detail` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84436)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `goods_detail` | [4:84436](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84436) | [4:84530](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84530) | [4:84505](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84505) | [4:84609](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-84609) |
| `goods_detail_other` | [49:10242](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10242) | [49:10346](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10346) | [49:10313](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10313) | [49:10427](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=49-10427) |

## 概要

機能目的:

- 1 つのグッズの情報と、そのグッズが登場した記録を見てもらう

機能概要:

- グッズの写真・名前・お迎え日・公式ページの URL の表示
- そのグッズに結び付いた記録の一覧
- グッズ情報の編集への導線

関連する機能：B-04、B-05

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | グッズと関連する記録を表示する |
| 2 | 公式ページ | リンク押下 | 公式ページを別のタブで開く |
| 3 | 関連する記録 | 項目押下 | [UIS14](../UIS14/README.md) へ遷移 |
| 4 | 情報を編集 | ボタン押下 | [UIS21](../UIS21/README.md) へ遷移 |
| 5 | わたしのグッズへ戻る | リンク押下 | [UIS18](../UIS18/README.md) へ遷移 |
| 6 | 投稿者の名前・アイコン | 項目押下 | [UIS23](../UIS23/README.md)（`user_posts`）へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| `goods_detail` | 記録の写真 | [UIS14](../UIS14/README.md)（`own_post_detail`） | 画面へ遷移 |
| `goods_detail_other` | 記録の写真 | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| `goods_detail` | 記録のひとこと | [UIS14](../UIS14/README.md)（`own_post_detail`） | 画面へ遷移 |
| `goods_detail_other` | 記録のひとこと | [UIS14](../UIS14/README.md)（`post_detail`） | 画面へ遷移 |
| 全状態 | 投稿者のアイコン | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| 全状態 | 投稿者名 | [UIS23](../UIS23/README.md)（`user_posts`） | 画面へ遷移 |
| `goods_detail` | 情報を編集 | [UIS21](../UIS21/README.md)（`goods_edit`） | 画面へ遷移 |
| `goods_detail` | わたしのグッズへ戻る | [UIS18](../UIS18/README.md)（`goods_list`） | 画面へ遷移 |

### 1. 初期表示

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| goods_id | 表示するグッズの ID | |

利用API:

| ID | 処理 | Parameter |
| --- | --- | --- |
| API42 | グッズを取得する | goods_id |
| API43 | グッズに結び付いた記録を取得する | goods_id |

画面表示制御:

- 本人のグッズの場合は、「情報を編集」を表示する
- 他の利用者のグッズの場合（[UIS14](../UIS14/README.md) のグッズを押した場合）は、グッズの情報と、そのグッズに結び付いた公開記録だけを表示する。非公開の記録は件数も出さない
- 他の利用者のグッズでは、「情報を編集」と「わたしのグッズへ戻る」を表示しない。サーバー側でも本人以外の更新を受け付けない（`goods_detail_other`）

### 3. 関連する記録

[UIS14](../UIS14/README.md) へ遷移する。

起動パラメータ:

| Name | Value | Memo |
| --- | --- | --- |
| post_id | 押した記録の ID | |

## 未確定事項

画面共通の事項は [一覧の未確定事項](../README.md#未確定事項画面全体) を参照。
