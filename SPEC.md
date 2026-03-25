# 全球大事件日历 - SPEC.md

## 1. Concept & Vision

一款专为手机设计的全球大事件日历，收录世界杯、奥运会清明节、国庆、演唱会等全球与中国重大事件。界面简洁有力，一眼看穿未来将要发生什么。深色主题，视觉冲击力强。

## 2. Design Language

- **Aesthetic**: 深色科技风，像一个新闻终端 + 赛事日历的结合体
- **Color palette**:
  - Background: #0a0a0f
  - Card background: #14141f
  - Primary accent: #f5c518 (金色，事件高亮)
  - Sports blue: #3b82f6
  - Festival red: #ef4444
  - Concert purple: #a855f7
  - Text primary: #ffffff
  - Text secondary: #8888aa
  - Border: #1e1e2e
- **Typography**: "Noto Sans SC" for Chinese, system-ui fallback
- **Motion**: 卡片hover微微上浮，列表项渐入动画
- **Icons**: Emoji 表情符号

## 3. Layout & Structure

- 手机优先（375px基准），PC端居中展示（max-width: 480px）
- 顶部：标题 + 当前月份导航
- 中部：月份切换按钮 + 日历网格
- 日历格：显示日期数字 + 当日事件标签（彩色小圆点/标签）
- 底部：当日事件详情列表
- 顶部有返回天气App的链接按钮

## 4. Features & Interactions

- 月份前后切换（左右箭头）
- 点击某个日期，底部展开该日事件列表
- **双层筛选功能**：
  - 事件类型筛选：全部 / 体育 / 中国节日 / 演出 / 全球 / 科技
  - 地理位置筛选：本市（杭州） / 本省（浙江） / 全国 / 全球
- 两个筛选维度同时生效，支持组合筛选
- 事件卡片显示地理范围标签
- 初始加载当前月份，当天有事件时自动高亮
- 数据硬编码在JS中（2026年全年事件）

## 5. Component Inventory

### 日历格子
- 默认：日期数字 + 底部事件圆点（最多3个）
- 今天：金色边框
- 有事件：事件类型对应彩色小标签
- 点击：背景高亮，底部展示详情

### 事件卡片
- 彩色标签（类型）+ 事件名称 + 时间/地点
- 分类颜色：
  - 体育赛事：#3b82f6
  - 中国节日：#ef4444
  - 全球节日：#f5c518
  - 演唱会/演出：#a855f7
  - 科技/其他：#22c55e

### 顶部导航
- 返回链接 + 标题 + 月份选择器

## 6. Technical Approach

- 纯HTML + CSS + JavaScript，单文件
- 无需构建，无依赖
- 数据结构：
```js
const events = [
  {
    id: 1,
    date: "2026-04-04",
    endDate: "2026-04-06",
    title: "清明节",
    type: "festival-china", // festival | sports | concert | global | tech
    locationScope: "national", // city | province | national | global
    location: "中国",
    description: "中华民族传统节日，祭祖踏青"
  },
  // ... more events
];
```

## 7. Events Data (2026)

### 体育
- 2026-02-17 to 2026-03-09: FIFA世界杯（美国/加拿大/墨西哥联合举办）
- 2026-05-30 to 2026-06-21: 温布尔登网球锦标赛（伦敦）
- 2026-07-03 to 2026-07-16: 温布尔登网球公开赛
- 2026-08-12 to 2026-08-24: 世界田径锦标赛（东京）
- 2026-09-25 to 2026-10-11: 亚运会（大阪）

### 中国节日
- 2026-01-01: 元旦
- 2026-01-28: 春节
- 2026-02-14: 情人节
- 2026-04-04 to 2026-04-06: 清明节
- 2026-05-01: 劳动节
- 2026-05-31: 母亲节
- 2026-06-12: 端午节
- 2026-06-21: 父亲节
- 2026-08-19: 中元节
- 2026-09-10: 中秋节
- 2026-10-01 to 2026-10-07: 国庆节
- 2026-10-25: 重阳节
- 2026-12-25: 圣诞节

### 全球节日
- 2026-01-01: 元旦（全球）
- 2026-02-14: 情人节
- 2026-03-14: 白色情人节
- 2026-04-01: 愚人节
- 2026-04-22: 地球日
- 2026-05-01: 国际劳动节
- 2026-06-05: 世界环境日
- 2026-07-14: 法国国庆日
- 2026-10-31: 万圣节
- 2026-11-11: 双十一购物节
- 2026-11-26: 感恩节
- 2026-12-24/25: 圣诞节

### 演唱会/演出
- 2026-03-15: Taylor Swift世界巡演 - 上海站
- 2026-04-10: Coldplay世界巡演 - 北京站
- 2026-05-01: 音乐节 - 迷笛音乐节（浙江）
- 2026-06-20: 周杰伦世界巡演 - 杭州站
- 2026-08-08: 张学友演唱会 - 上海站
- 2026-11-15: 五月天演唱会 - 北京站

### 科技/其他
- 2026-03-25: 苹果春季发布会
- 2026-06-08: WWDC2026（苹果全球开发者大会）
- 2026-09-15: 苹果秋季发布会
- 2026-11-10: 双十一购物节
- 2026-12-12: 双十二购物节

### 地理范围标注 (locationScope)

- **city (本市/杭州)**: 杭州马拉松、Coldplay北京站（实际改为杭州）、周杰伦杭州站等
- **province (本省/浙江)**: 迷笛音乐节（浙江）
- **national (全国)**: Taylor Swift上海站、Coldplay北京站、张学友上海站、五月天北京站、春节、清明节、国庆节、双十一、双十二
- **global (全球)**: FIFA世界杯、温布尔登、苹果发布会、WWDC、圣诞节、万圣节、亚运会

---

## Important Implementation Notes

- Deploy to GitHub Pages at: https://github.com/boyzhoulei-del/event-calendar/
- After creating the files, commit and push to GitHub
- Enable GitHub Pages in repo settings

## Output files to create:
- /Users/zhoulei/.qclaw/workspace/event-calendar/SPEC.md
- /Users/zhoulei/.qclaw/workspace/event-calendar/index.html