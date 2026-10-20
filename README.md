# 感覚ラボ

公開URL：https://minolu-29.github.io/kankaku-lab/

あなたの感覚は何%正確？ 色・角度・リズム・時間感覚など、自分の感覚の精度を測る20代向けのミニゲーム10本。1回1分ほどで終わり、結果は画像にしてXやストーリーにシェアできます。

## ゲーム一覧

| # | ゲーム | 内容 | リンク |
|---|---|---|---|
| 01 | 色の記憶 | 2秒だけ見た色を、パレットから再現する | `#color` |
| 02 | 角度ピタリ | 目盛りなしで、指定の角度に線を回す | `#angle` |
| 03 | まんなかタップ | いびつな図形の重心をタップ | `#center` |
| 04 | 長さコピー | 一瞬見た線と同じ長さを指で引く | `#length` |
| 05 | テンポキープ | 4拍のリズムを覚え、無音で8回刻み続ける | `#tempo` |
| 06 | 一瞬の個数 | 0.7秒だけ出る点の数を当てる | `#count` |
| 07 | 体内時計 | 指定の秒数だけ押し続ける | `#hold` |
| 08 | ちがいの限界 | 大きいほうを選び続け、見分けられる最小の差を測る | `#jnd` |
| 09 | 光についていけ | 動き回る光に指をのせ続ける | `#trace` |
| 10 | リングタップ | 縮む輪が円に重なった瞬間にタップ（40ノーツ） | `#ring` |

URLの末尾に `#color` などを付けると、そのゲームが直接開きます。

## しくみ（どこを直せば何が変わるか）

ゲーム本体は `src/index.html` の1ファイルだけです。ここを直して main に入れると、GitHub が自動で次の3つを作り直します。

| 作られるもの | 置き場所 | 使い道 |
|---|---|---|
| 自分のサイト版 | GitHub Pages（公開URL） | 広告（Google）とアクセス解析つき |
| `kankaku-lab-crazygames.zip` | Releases の「latest」 | CrazyGames にアップロード |
| `kankaku-lab-gamedistribution.zip` | Releases の「latest」 | GameDistribution にアップロード |

広告やアクセス解析のIDは `monetize.config.json` に書きます。空のあいだは広告なしで動きます。

| 項目 | 入れるもの |
|---|---|
| `web.adsenseClient` | AdSense のサイト運営者ID（`ca-pub-` で始まる） |
| `web.adTest` | 審査中・確認中は `true`（テスト広告）。本番は `false` |
| `web.ga4` | Google アナリティクスの測定ID（`G-` で始まる） |
| `gamedistribution.gameId` | GameDistribution でゲームを登録したときにもらうID |
| `customDomain` / `siteUrl` | 独自ドメインを使うときに設定 |

画面の文字は、ブラウザが日本語なら日本語、それ以外は英語で出ます。ホーム画面の下のボタンで切り替えられ、URLに `?lang=en` を付けても英語になります。

## ファイル

| ファイル | 役割 |
|---|---|
| `src/index.html` | ゲーム本体（HTML・CSS・JSを1ファイルに収録） |
| `src/platforms/` | 配信先ごとの違い（広告の出し方・記録の保存先）だけをまとめたファイル |
| `tools/build.mjs` | 配信先ごとの版を `dist/` に作るスクリプト（`node tools/build.mjs`） |
| `monetize.config.json` | 広告・解析・配信先のID |
| `public/` | アイコン・SNS用プレビュー画像など、サイトにそのまま置くファイル |
| `store/` | ゲームサイトに提出するカバー画像 |
| `.github/workflows/publish.yml` | 自動で作り直して公開する設定 |

ベスト記録と音のオン・オフは、その端末のブラウザ（CrazyGamesではアカウント）に保存されます。
