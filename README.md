# ⚡ Serpens Main Board

> Main control board project for the Serpens snake-shaped pet robot.

Serpens本体の制御系を統合するために設計している
**メイン制御基板プロジェクト**です。

将来的に、

- MCU
- 電源
- サーボバス
- センサ接続
- 通信
- 安全系

を1枚の基板へまとめることを目指しています。

> ⚠️ 現在は初期設計段階です。  
> 完成基板・製造済み基板・実機動作確認済みの回路はまだありません。

---

## 🎯 Purpose

Serpensでは、

```text
Sensors
↓
Main Controller
↓
Motion / Behavior
↓
Servo Bus
↓
Actuators
```

という構成を想定しています。

この基板は、
Serpens全体の電子回路・制御系をまとめる
中心的なハードウェアになる予定です。

---

## 🧩 Current Status

| Area | Status |
|---|---|
| Requirements | 🟡 In progress |
| System architecture | 🟡 In progress |
| MCU selection | 🟡 Under consideration |
| Power design | 🟡 Under consideration |
| Servo bus interface | 🟡 Under consideration |
| Sensor interfaces | 🟡 Under consideration |
| Schematic | 🔴 Early stage |
| PCB layout | 🔴 Early stage |
| DRC / ERC | ⚪ Not completed |
| Gerber | ⚪ Not generated |
| Manufacturing | ⚪ Not ordered |
| Hardware verification | ⚪ Not tested |

現時点では、
基板全体の構成検討と初期設計を進めています。

---

## 🏗 Planned Architecture

想定している構成：

```text
Battery / Power
      ↓
Power Regulation
      ↓
     MCU
   ↙  ↓  ↘
Sensors  Servo Bus  Communication
             ↓
         Actuators
```

今後、
Serpensの実機構成に合わせて
電源・通信・安全設計を具体化していきます。

---

## ⚙️ Planned Functions

将来的に統合したい機能：

- Main MCU
- Servo bus communication
- Sensor interfaces
- Power distribution
- Voltage monitoring
- Current monitoring
- Communication with PC / upper controller
- Emergency / safety-related interfaces
- Expansion connectors

実際の回路仕様は、
Serpens本体側の設計と合わせて変更する可能性があります。

---

## 🛡 Safety Considerations

Serpensでは、
PC側だけに安全を依存しない構成を目指しています。

メイン基板でも今後、

- Communication watchdog
- Power monitoring
- Emergency stop path
- Safe startup state
- Servo enable / disable
- Fault detection

などを検討します。

ただし、
これらは現時点で実装済みではありません。

---

## 🧠 Design Approach

この基板では、

```text
Requirement
↓
Architecture
↓
Schematic
↓
PCB Layout
↓
ERC / DRC
↓
Fabrication
↓
Bring-up
↓
Hardware Verification
```

の順で設計を進めます。

完成した回路だけを見せるのではなく、

- 仮定
- 未確認事項
- 設計判断
- 検証結果

を分けて管理することを重視しています。

---

## 🛠 Tools

- KiCad
- Git / GitHub
- BoardRepo

---

## 📂 Repository Structure

```text
snake-main-board/
├─ *.kicad_pro
├─ *.kicad_sch
├─ *.kicad_pcb
│
├─ libs/
│  └─ Custom symbols / footprints
│
├─ 3dmodels/
│  └─ STEP models
│
├─ fabrication/
│  └─ Gerber / Drill / BOM / Position files
│
└─ docs/
   └─ Schematics / design notes / component selection
```

KiCadプロジェクト本体は
リポジトリ直下に配置します。

---

## 🔄 Version Control

この基板は、

- GitHub
- BoardRepo

を併用して管理しています。

GitHubではファイル・履歴を管理し、
BoardRepoではPCB設計のVisual Diffや
レビュー用途での活用を想定しています。

---

## 🚧 Current Limitations

現在は以下が未完了です。

- Complete schematic
- Power architecture
- Final MCU selection
- Servo bus circuit
- Sensor interface design
- PCB routing
- ERC / DRC verification
- Fabrication outputs
- Manufacturing
- Hardware bring-up
- Real robot integration

---

## 🛠 Next Steps

1. Serpens全体の電源・制御要件を整理
2. MCU / communication architecture決定
3. Servo bus interface設計
4. Sensor interface設計
5. Power circuit設計
6. Schematic completion
7. ERC
8. PCB layout
9. DRC
10. Gerber generation
11. Manufacturing
12. Bring-up / hardware verification

---

## 📌 Project Status

**Early hardware design stage**

Serpensの機械設計・ソフトウェア・センサ基板と並行して、
ロボット全体を統合するためのメイン基板を設計しています。

現時点では完成基板ではなく、
これから実装・製造・実機検証へ進むR&Dプロジェクトです。
