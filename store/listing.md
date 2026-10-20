# ゲームサイト提出用テキスト

提出フォームは英語なので、英語の文をそのままコピーして使ってください。日本語訳は確認用です。
アップロードするファイルとカバー画像は、GitHub の Releases「latest」に自動で置かれます。

## 感覚ラボ（kankaku-lab）

**Title**
Sense Lab - How Accurate Are You?

**Description（英語）**
How accurate are your senses? Sense Lab measures them with 10 short tests. Remember a color for two seconds and recreate it, rotate a line to an exact angle without a scale, tap the center of mass of odd shapes, keep a tempo in silence, guess how many dots flashed on screen, hold for exactly 3.4 seconds, follow a moving light, and hit shrinking rings in a rhythm round. Your result is shown as a percentage, so you always know how close you were.

（日本語訳）あなたの感覚は何%正確？色の記憶、角度ピタリ、まんなかタップ、テンポキープ、一瞬の個数、体内時計、光についていけ、リングタップなど10種類の感覚テスト。結果は精度%で表示されます。

**Controls**
- Tap, drag or hold depending on the test. Each test explains what to do before it starts.
- Works with mouse and touch.

**Category / Tags（候補）**
Casual / skill, reaction, color, rhythm, brain, test

## CrazyGames の設定
| 項目 | 設定 |
|---|---|
| Game file | `kankaku-lab-crazygames.zip` をアップロード |
| Orientation（画面の向き） | Portrait（縦）。パソコンでも左右に余白が付いて遊べます |
| Mobile support | Yes（スマホ・タブレット対応） |
| Progress Save（記録の保存） | **必ずオンにする**。オフだとベスト記録が保存されません |
| Covers | `store/` の3枚（1920×1080・800×1200・800×800） |
| Language | English, Japanese（ブラウザの言語で自動切り替え） |

## GameDistribution の設定

1. ゲームを新規登録して、もらった Game ID を `monetize.config.json` の `gamedistribution.gameId` に入れて main に入れる
2. 数分後に Releases「latest」に作り直される `kankaku-lab-gamedistribution.zip` をアップロードする
3. タイトル・説明文・操作方法は上と同じ英語を使う。画面の向きは Portrait、スマホ対応は Yes
