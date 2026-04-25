# 🎮 跑酷游戏 — SPEC.md

## 1. Concept & Vision

一款极简风格的无限跑酷游戏。玩家控制一个小人向前奔跑，点击/按键跳跃躲避障碍物。目标是活得更久、分数更高。风格：霓虹夜晚的城市天际线，动感十足，一玩就停不下来。

## 2. Design Language

- **Aesthetic**: 赛博朋克霓虹风，深色背景配亮色线条
- **Colors**:
  - Background: #0a0a1a (深夜蓝黑)
  - Ground: #1a1a3a (暗紫)
  - Player: #00f5d4 (青色霓虹)
  - Obstacle: #ff2d55 (红色霓虹)
  - Coin/Collectible: #ffd60a (金色)
  - Text: #ffffff
  - Accent: #7b2ff7 (紫色)
- **Typography**: System UI / sans-serif，简洁有力
- **Motion**: 60fps 流畅动画，跳跃有物理感（抛物线），障碍物匀速接近

## 3. Layout & Structure

- 全屏 Canvas，适配手机和桌面
- 顶部：分数 + 最高分
- 底部：地面跑道
- 中央（游戏结束后）：重新开始界面 + 分数展示

## 4. Features & Interactions

- **操作**：
  - 手机：点击屏幕任意位置跳跃
  - 桌面：空格键或 ↑ 跳跃
- **障碍物**：随机生成的红柱子和从天而降的障碍
- **收集**：金色星星，碰到+10分
- **死亡**：碰到障碍物游戏结束
- **难度递增**：每存活10秒，速度增加10%
- **最高分**：存储在 localStorage

## 5. Component Inventory

- **Player**：40x40 像素方块，带霓虹描边
- **Ground**：地面线条，往左移动形成跑动感
- **Obstacle**：红色竖条 or 圆形
- **Coin**：旋转金色星星
- **Game Over Screen**：半透明遮罩 + 分数 + 重新开始按钮

## 6. Technical

- 单 HTML 文件，内嵌 CSS + JavaScript
- Canvas 2D 渲染，requestAnimationFrame
- 触摸事件 + 键盘事件
- localStorage 存储最高分
