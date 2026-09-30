# snake-main-board

**蛇ロボット（Serpens）のメイン基板**の KiCad プロジェクト。

- 基板名: `snake-main-board`
- 用途: 蛇ロボットのメイン基板（MCU・電源・サーボバス・センサー接続）
- バージョン管理: GitHub（プライベート）+ [BoardRepo](https://boardrepo.com)（Visual Diff）

## フォルダ構成

| 場所 | 中身 |
|---|---|
| `（このフォルダ直下）` | **KiCad プロジェクト（`.kicad_pro` / `.kicad_sch` / `.kicad_pcb`、階層シート、`fp-lib-table` / `sym-lib-table`）** |
| `libs/` | 自作のシンボル（`.kicad_sym`）・フットプリント（`.pretty/`） |
| `3dmodels/` | 3D モデル（`.step`）。フットプリントからは相対パスで参照する |
| `fabrication/` | 製造データ（ガーバー、ドリル、BOM、部品配置ファイル） |
| `docs/` | 回路図の PDF、設計メモ、部品選定の根拠 |

**KiCad プロジェクトはこのフォルダ直下に置く**（`libs/` などの下ではない）。

## 注意

- `*-backups/`、`fp-info-cache`、`*.kicad_prl`、ロックファイル、自動保存は Git に入れない（`.gitignore`）。
- 空のフォルダを Git に残すため、`libs/` `3dmodels/` `fabrication/` `docs/` に `.gitkeep` を置いてある（中身が入ったら消してよい）。
- このフォルダは、親の `serpens`（ロボット制御のリポジトリ）とは**別の Git リポジトリ**にする（入れ子）。親側は `.git/info/exclude` で無視する。
