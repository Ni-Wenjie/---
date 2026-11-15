# CYBER DECK · 赛博扑克牌

> 以一套经典扑克牌为基础再铸的赛博朋克风格卡牌。54 张正牌 + 卡背，PNG 透明圆角，可直接替换原牌使用。

![preview](preview.png)

## 这是什么

原牌是干净的黑白红经典版式，这里把它翻成**霓虹双极**（Cyber Neon Duotone）：深空暗场打底，墨迹变成霓虹灯管，再叠一层设备面板式的 HUD 信息层。rank 字形、pip 排布、人像线稿、卡背斜向网纹全部沿用原牌，只换视觉皮肤——所以它是同一副牌的另一套皮，不是另一副牌。

## 四色霓虹花色

| 花色 | 主色 | HEX | 协议代号 |
|---|---|---|---|
| ♠ Spade | 冰青 | `#00E5FF` | ICE-PROTOCOL |
| ♥ Heart | 品红 | `#FF2E97` | CORE-PULSE |
| ♣ Club | 离子紫 | `#8B5CFF` | NODE-GRID |
| ♦ Diamond | 数据琥珀 | `#FFB028` | DATA-SHARD |

## 目录结构

```
.
├─ cards/             # 54 张正牌：Spade2…SpadeA、Heart2… 、JOKER-A / JOKER-B
├─ card-back.png      # 卡背
├─ preview.png        # 全牌总览
├─ hero.png           # 扇形主视觉
├─ breakdown.png      # 单牌设计拆解
├─ build_cyber_deck.py   # 全牌生成脚本（可复现 / 可换色）
└─ make_presentation.py  # 呈现图生成脚本
```

## 规格

- 尺寸 750 × 1044 px，300 DPI 约合 63.5 × 88.4 mm，与原套牌 1:1 对齐
- RGBA PNG，圆角半径 30 px，卡外区域透明
- 命名沿用原套牌，`cards/Spade2.png` 直接覆盖同名文件即可替换

## 整副换色

改 `build_cyber_deck.py` 顶部的 `SUITS` 字典重跑即可，54 张一次生效：

```bash
python build_cyber_deck.py full     # 全套 54 张 + 卡背
python build_cyber_deck.py test     # 4 张试色
```

## 打印前请注意

- 现为 RGB，上机印刷需转 CMYK 并重新校色；深底大面积网点建议先试印
- HUD 小字仅 11 px（约 0.9 mm），量产建议放大到 14 px 或改压印
- 推荐 350 g 黑芯卡纸 + 局部 UV / 烫镭射，卡框线才出灯管质感

## 许可

未指定开源许可。转载、商用或二次分发前请先与作者确认。
