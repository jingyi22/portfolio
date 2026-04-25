# 香港演唱会票务平台 UX 优化 Demo — SPEC.md

## 1. Concept & Vision

基于 Trip.com 演唱会门票竞品测试研究，针对票券冒领问题设计优化方案展示。风格与 07_AI_Chatbot_Feedback 保持一致：深色科技感、数据驱动、专业的 UX 研究报告风格。通过手机模拟界面展示改进后的购票流程。

## 2. Design Language

- **Aesthetic**: 深色科技风（Dark Mode），参考 GitHub/Linear 的专业感
- **Colors**:
  - Primary: #1B6EFD (蓝色)
  - Background: #0D1117
  - Card BG: #161B22
  - Border: #30363D
  - Text: #E6EDF3
  - Text Secondary: #8B949E
  - Green: #2EA043 (解决)
  - Red: #F85149 (问题)
  - Orange: #F0883E (部分解决)
  - Yellow: #D29922 (待观察)
- **Typography**: DM Serif Display (标题) + Inter (正文)
- **Motion**: 简洁过渡，0.2-0.3s ease

## 3. Layout & Structure

- **Introduction Page (Hero)**:
  - 项目标题 + 背景说明
  - 核心数据统计（测试平台数、演唱会场次、问题数）
  - 三大核心问题卡片

- **Key Findings Section**:
  - 4个主要问题（政策不明确、确认环节弱、免责条款弱、订单管理弱）
  - 对比竞品优秀实践

- **UI Demo Section**:
  - 手机模拟框架展示优化后的购票流程
  - 4个关键改进点的界面展示

## 4. Demo Screens (Phone Mockup)

### Screen 1: 票务详情页（优化后）
- 醒目的"购票政策"标签（红色警告风格）
- 关键信息突出显示
- 信息填写前弹窗提醒

### Screen 2: 信息确认页（新增）
- 独立的信息核对页面
- 逐项勾选确认框
- 免责条款清晰展示

### Screen 3: 订单确认页
- 信息二次确认
- 隐藏取票码
- 防截图提示

### Screen 4: 订单管理页
- 取票码部分隐藏显示
- 票券安全提示
- 不可重复使用提示

## 5. Technical

- 单 HTML 文件，无外部依赖（除 Google Fonts）
- Vanilla JS 实现交互（点击切换屏幕）
- CSS 变量统一管理颜色
- 手机模拟框架使用 iframe 或 CSS 模拟
