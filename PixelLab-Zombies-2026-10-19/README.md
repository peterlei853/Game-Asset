# PixelLab Zombies — PixelLab-Zombies-2026-10-19

遊戲用僵屍角色像素動畫，由 PixelLab MCP 生成（`animate_character`, mode = `pixminimax`），
批次日期 2026-10-19。

## 內容

- **角色**：5 個
- **動畫**：50 段（每角色 10 段）
- **總幀數**：713 幀
- **方向**：全部 `east`（單向）
- **格子尺寸**：84×84 或 88×88（見各動畫 `meta.json` 的 `cell`）

## 目錄結構

```
PixelLab-Zombies-2026-10-19/
├── manifest.json              全批次索引（角色 → 動畫 → 幀數 / 路徑）
├── README.md
└── Zombie02-Normal/
    ├── character.json         該角色的動畫清單與 PixelLab character id
    └── die-critical-hit/
        ├── frames/000.png …   逐幀 PNG（含透明通道）
        ├── sheet.png          水平 sprite strip，cell 寬 × 幀數
        └── meta.json          幀數、cell、來源、修剪紀錄
```

## 動畫清單

| 角色 | 動畫 | 幀數 | cell |
|---|---|---|---|
| Zombie02-Normal | Die-critical hit | 29  (原 33，已刪開頭 4) | 84x84 |
| Zombie02-Normal | Die-disappear | 12  (原 33，已刪開頭 21) | 84x84 |
| Zombie02-Normal | Die-deathwalk | 30  (原 33，已刪開頭 3) | 84x84 |
| Zombie02-Normal | Die-normal01 | 7  (原 8，已刪開頭 1) | 84x84 |
| Zombie02-Normal | Die-normal02 | 6  (原 8，已刪開頭 2) | 84x84 |
| Zombie02-Normal | hit01-normal | 16 | 84x84 |
| Zombie02-Normal | hit02-normal | 16 | 84x84 |
| Zombie02-Normal | Hurt-normal | 4 | 84x84 |
| Zombie02-Normal | Walk-normal | 8 | 84x84 |
| Zombie02-Normal | Walk-TireMove | 8 | 84x84 |
| Zombie03-Normal | Die-critical hit | 30  (原 33，已刪開頭 3) | 84x84 |
| Zombie03-Normal | Die-disappear | 21  (原 33，已刪開頭 12) | 84x84 |
| Zombie03-Normal | Die-deathwalk | 29  (原 33，已刪開頭 4) | 84x84 |
| Zombie03-Normal | Die-normal01 | 6  (原 8，已刪開頭 2) | 84x84 |
| Zombie03-Normal | Die-normal02 | 7  (原 8，已刪開頭 1) | 84x84 |
| Zombie03-Normal | hit01-normal | 16 | 84x84 |
| Zombie03-Normal | hit02-normal | 16 | 84x84 |
| Zombie03-Normal | Hurt-normal | 4 | 84x84 |
| Zombie03-Normal | Walk-normal | 8 | 84x84 |
| Zombie03-Normal | Walk-TireMove | 8 | 84x84 |
| Zombie04-Normal | Die-critical hit | 32  (原 33，已刪開頭 1) | 84x84 |
| Zombie04-Normal | Die-disappear | 27  (原 33，已刪開頭 6) | 84x84 |
| Zombie04-Normal | Die-deathwalk | 26  (原 33，已刪開頭 7) | 84x84 |
| Zombie04-Normal | Die-normal01 | 7  (原 8，已刪開頭 1) | 84x84 |
| Zombie04-Normal | Die-normal02 | 7  (原 8，已刪開頭 1) | 84x84 |
| Zombie04-Normal | hit01-normal | 16 | 84x84 |
| Zombie04-Normal | hit02-normal | 16 | 84x84 |
| Zombie04-Normal | Hurt-normal | 4 | 84x84 |
| Zombie04-Normal | Walk-normal | 8 | 84x84 |
| Zombie04-Normal | Walk-TireMove | 8 | 84x84 |
| Zombie10-Normal | Die-critical hit | 22  (原 33，已刪開頭 11) | 88x88 |
| Zombie10-Normal | Die-disappear | 21  (原 33，已刪開頭 12) | 88x88 |
| Zombie10-Normal | Die-deathwalk | 32  (原 33，已刪開頭 1) | 88x88 |
| Zombie10-Normal | Die-normal01 | 5  (原 8，已刪開頭 3) | 88x88 |
| Zombie10-Normal | Die-normal02 | 7  (原 8，已刪開頭 1) | 88x88 |
| Zombie10-Normal | hit01-normal | 16 | 88x88 |
| Zombie10-Normal | hit02-normal | 16 | 88x88 |
| Zombie10-Normal | Hurt-normal | 4 | 88x88 |
| Zombie10-Normal | Walk-normal | 8 | 88x88 |
| Zombie10-Normal | Walk-TireMove | 8 | 88x88 |
| Zombie-normal06 | Die-critical hit | 27  (原 33，已刪開頭 6) | 84x84 |
| Zombie-normal06 | Die-disappear | 20  (原 33，已刪開頭 13) | 84x84 |
| Zombie-normal06 | Die-deathwalk | 29  (原 33，已刪開頭 4) | 84x84 |
| Zombie-normal06 | Die-normal01 | 7  (原 8，已刪開頭 1) | 84x84 |
| Zombie-normal06 | Die-normal02 | 7  (原 8，已刪開頭 1) | 84x84 |
| Zombie-normal06 | hit01-normal | 16 | 84x84 |
| Zombie-normal06 | hit02-normal | 16 | 84x84 |
| Zombie-normal06 | Hurt-normal | 4 | 84x84 |
| Zombie-normal06 | Walk-normal | 8 | 84x84 |
| Zombie-normal06 | Walk-TireMove | 8 | 84x84 |

## 兩組動畫的差別

**死亡組（`die-*`）** — 先由 PixelLab 生成 33 / 8 幀，再本地移除開頭冗餘幀。
`meta.json` 保留了完整可追溯資訊：

- `original_frames` — 原始幀數
- `dropped_leading` — 刪掉的開頭幀數
- `cut_reason` — `static idle lead-in`（靜止待機）或 `walk-cycle lead-in`（模型自行加上的走路段）
- `frame_index_map` — 修剪後每一幀對應的原始幀索引

也就是說 `frames/000.png` 不等於原始 `000.png`，要對照原始素材請查 `frame_index_map`。

**戰鬥／行走組（`hit*` / `hurt` / `walk*`）** — 直接以目標幀數生成，未經修剪，
`frame_index_map` 不存在，索引與原始輸出一致。

幀數全部為 4 的倍數（PixMiniMax 的硬限制：`frame_count` 必須是 4–40 之間的 4 的倍數）。
生成時 `keep_first_frame=false`，所以不會多插一張站立參考幀。

## 已知品質問題

- `hit02-normal` 部分角色約有一半是靜止幀（如 Zombie10 的 f00–f02 與 f09–f15 完全不動），
  實際揮擊只有中間 6 幀。若要進遊戲建議再剪一次。
- `hurt-normal` 只有 4 幀，模型直接從受擊瞬間開始，沒有「後仰 → 血花 → 回正」的鋪陳。

## 授權

素材由 PixelLab 生成，使用權依 PixelLab 訂閱條款。角色設計為本專案原創。
