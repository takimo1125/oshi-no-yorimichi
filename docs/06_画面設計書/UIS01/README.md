# [UIS01] トップページ（LP）

Figma で開く: [`lp` の PC](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-80731)

Figma のフレーム:

| 画面モデル | PC | スマホ | 説明 PC | 説明 スマホ |
| --- | --- | --- | --- | --- |
| `lp` | [4:80731](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-80731) | [4:80963](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-80963) | [4:80930](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-80930) | [4:81148](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-81148) |
| `lp_categories_vertical` | — | [4:98447](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98447) | — | [4:98626](https://www.figma.com/design/AUNEBoh9AdHbRHwHsyQaHJ/%E6%8E%A8%E3%81%97%E3%81%AE%E3%82%88%E3%82%8A%E3%81%BF%E3%81%A1%EF%BC%88%E6%94%B9%E5%96%84%E6%A1%88%EF%BC%89?node-id=4-98626) |

## 概要

機能目的:

- サービスを知らない人に、何ができるかを伝え、登録・閲覧へ導く

機能概要:

- サービスの紹介（日々の記録・テーマ展示・公開範囲・週末便などのお知らせ・はじめ方）
- 料金の案内（無料 0 円・展示プラス月額 300 円）
- 登録・ログイン・ホームの閲覧への導線
- 規約類への導線

関連する機能：H-05

## イベント概要

| No | イベント名 | イベント分類 | 処理説明 |
| --- | --- | --- | --- |
| 1 | 初期表示 | 初期表示 | 紹介用の固定の内容を表示する |
| 2 | みんなのよりみちをのぞいてみる | ボタン押下 | [UIS09](../UIS09/README.md) へ遷移 |
| 3 | 無料ではじめる | ボタン押下 | [UIS02](../UIS02/README.md) へ遷移 |
| 4 | ログイン | リンク押下 | [UIS05](../UIS05/README.md) へ遷移 |
| 5 | 楽しみ方・料金 | リンク押下 | Figma のリンクは同じ LP（`lp`）へ遷移。ページ内のスクロール位置は未確定 |
| 6 | 記録・展示の見本 | 項目押下 | 記録の見本は [UIS09](../UIS09/README.md)、展示の見本は [UIS29](../UIS29/README.md) へ遷移 |
| 7 | 料金のプラン | 項目押下 | 無料は [UIS02](../UIS02/README.md)、展示プラスは [UIS38](../UIS38/README.md) へ遷移 |
| 8 | 規約類 | リンク押下 | [UIS46](../UIS46/README.md)・[UIS47](../UIS47/README.md)・[UIS48](../UIS48/README.md) へ遷移 |

## イベント詳細

### Figma の操作と遷移

共通ナビゲーションは [画面共通の動き](../README.md#全画面で共通の動き) を参照。表はリンクが設定された操作を示す。リンクのない操作の処理・未確定事項は後述する。

| 画面モデル | 操作 | 遷移先・状態 | 表示方法 |
| --- | --- | --- | --- |
| 全状態 | 画像 | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |
| 全状態 | みんなのよりみちをのぞいてみる | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |
| 全状態 | 無料ではじめる | [UIS02](../UIS02/README.md)（`signup`） | 画面へ遷移 |
| 全状態 | 写真はないけど、今日の配信がよかった。 | [UIS09](../UIS09/README.md)（`home`） | 画面へ遷移 |
| 全状態 | 展示の見本 | [UIS29](../UIS29/README.md)（`exhibition_detail`） | 画面へ遷移 |
| 全状態 | 展示の見本の写真 | [UIS29](../UIS29/README.md)（`exhibition_detail`） | 画面へ遷移 |
| 全状態 | Plan プラン/無料 | [UIS02](../UIS02/README.md)（`signup`） | 画面へ遷移 |
| 全状態 | Plan プラン/展示プラス | [UIS38](../UIS38/README.md)（`plus_inactive`） | 画面へ遷移 |
| 全状態 | 利用規約 | [UIS46](../UIS46/README.md)（`terms`） | 画面へ遷移 |
| 全状態 | プライバシーポリシー | [UIS47](../UIS47/README.md)（`privacy`） | 画面へ遷移 |
| 全状態 | 特定商取引法に基づく表記 | [UIS48](../UIS48/README.md)（`commerce`） | 画面へ遷移 |
| `lp_categories_vertical`（スマホ） | ロゴ | 同じ画面（`lp`） | 状態の切り替え |

### 1. 初期表示

起動パラメータ：なし

利用API：なし。紹介の内容と見本の写真は固定で持つ

画面表示制御:

- ログイン済みで開いた場合の動きは未確定

### 2. みんなのよりみちをのぞいてみる

[UIS09](../UIS09/README.md) へ遷移する。ヒーローの直後と料金の節の後の 2 か所に置く。

### 3. 無料ではじめる

[UIS02](../UIS02/README.md) へ遷移する。ヒーローの直後に置く。

### 6. 記録・展示の見本

見本は固定の内容で、実在の記録・展示ではない。展示の見本から [UIS29](../UIS29/README.md) へ進む場合に、どの展示を表示するかは未確定。

### 7. 料金のプラン

展示プラスを押した場合、未ログインなら [UIS05](../UIS05/README.md) を経由して [UIS38](../UIS38/README.md) へ進む。

## 未確定事項

- スマホでのカテゴリーの並べ方は、横並び（`lp`）を標準とする。縦並び（`lp_categories_vertical`）は比較用の案で、違和感があれば戻す
