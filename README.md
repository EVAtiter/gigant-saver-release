# GigantSaver

レトロフューチャー計器の液体メーターを表示する macOS スクリーンセーバー。

![GigantSaver](images/screenshot.png)

## 概要

スクリーンセーバー版の `Gigant Monitor`。液体メーター描画ルーチン
(IndustriaMeter) を流用し、画面いっぱいに巨大な計器を映す。

壁から滲み出して右へ流れるボール、伸びて千切れる液体のネック、過負荷時の赤いギザギザ
波形 — 1970 年代後半の SF アニメ (『未来少年コナン』のインダストリア司令室の計器盤
など) へのオマージュとして、デスクトップを 1 つの巨大計器に変える。

## 機能

- **液体メーターの段階遷移描画**
  値に応じて 壁 → ボール → 千切れサテライト → ギザギザ波形 → 過負荷の赤色化 が
  シームレスに遷移
- **テーマ 10 種**: AmberCRT / Aurora / Blueprint / Glacier / Modern / Retro / Showa /
  SlateDusk / Smoke / Sumi
- **色サイクル機能** (任意)
  CPU(紫) → 電力(赤) → Network(緑) → Disk(青) を時間で巡回。Network / Disk は方向
  ランダム化 (上り/下り、書込/読込)。切替周期は 15 秒〜5 分から選択
- **画面サイズ非依存の描画**
  仮想幅 900pt 基準で描画して実画面サイズへ拡縮するため、どのモニター解像度でも
  比率が一定の見た目になる
- **マルチディスプレイ対応**
  各画面ごとに独立した状態で描画 (per-view state)

## 動作環境

- macOS 14 (Sonoma) 以上
- Apple Silicon または Intel (Universal Binary)

## インストール

### Homebrew Cask (推奨)

```bash
brew install --cask EVAtiter/tap/gigant-saver
```

### 手動

1. [最新の zip をダウンロード](https://github.com/EVAtiter/gigant-saver-release/releases/latest)
2. zip を展開
3. `GigantSaver.saver` をダブルクリック
4. システム設定 → 壁紙 → スクリーンセーバ → "GigantSaver" を選択

## 設定

システム設定 → 壁紙 → スクリーンセーバ → GigantSaver → **オプション...** から:

| 設定項目 | 内容 |
|---|---|
| テーマ | 10 種類から選択 |
| アニメ速度 | ゆっくり (0.5x) / 標準 (1.0x) / 高速 (1.5x) |
| 色を順に切り替え | CPU → 電力 → Network → Disk を周期的に切替 |
| 切替周期 | 15 秒 / 30 秒 / 1 分 / 3 分 / 5 分 |

## 著作権・ライセンス

Copyright © 2026 EVA Titer. All rights reserved.

公証済み Developer ID 署名バイナリとして配布。Gatekeeper を通過します。

## バージョン履歴

各バージョンの変更点は [Releases](https://github.com/EVAtiter/gigant-saver-release/releases)
を参照。
