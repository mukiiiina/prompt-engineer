# Example: Mobile Fitness Tracker App Prompt

A cross-platform mobile app prompt demonstrating the Mobile App template (Template D) with React Native + Expo.

---

## Generated Prompt (English)

You are a senior mobile developer. Build a cross-platform fitness tracking application.

## 1. App Overview

- **App Name**: FitPulse
- **Platform**: iOS and Android
- **Framework**: React Native 0.73 + Expo SDK 50
- **App Category**: Health & Fitness
- **Core Purpose**: Help users track workouts, monitor health metrics, and achieve fitness goals with AI-powered insights
- **Target Users**: Fitness enthusiasts aged 18-45, gym-goers, runners, home workout practitioners

## 2. Screens

| Screen | Purpose | Key UI |
|--------|---------|--------|
| Onboarding | User setup | Goal selection, fitness level, preferences |
| Home/Dashboard | Daily overview | Today's workout, activity rings, streak counter |
| Workout | Exercise tracking | Timer, set/rep counter, rest timer, exercise list |
| History | Past workouts | Calendar view, workout list, stats summary |
| Progress | Long-term trends | Charts (weight, strength, endurance), photo comparison |
| Profile | User settings | Goals, preferences, connected devices, subscription |
| Social | Community | Friend list, leaderboards, challenges, share workout |

## 3. Navigation

- **Structure**: Bottom Tab Navigator (5 tabs: Home, Workout, History, Social, Profile)
- **Stack screens**: Onboarding -> Main Tabs, Workout Detail, Exercise Library, Settings
- **Deep linking**: `fitpulse://workout/123`, `fitpulse://challenge/abc`
- **Modal**: Exercise picker, rest timer overlay, share sheet

## 4. State Management

- **Global state**: Zustand (user profile, workout data, preferences)
- **Local state**: useState/useReducer (form inputs, UI toggles)
- **Persistence**: AsyncStorage (auth token, user preferences), SecureStore (credentials)
- **Cache**: React Query (server data, workout history)
- **Background tasks**: expo-background-fetch (sync health data when app closed)

## 5. Native Features

| Feature | Implementation | Purpose |
|---------|---------------|---------|
| HealthKit / Google Fit | `expo-health-connect` | Sync steps, heart rate, calories |
| GPS Tracking | `expo-location` | Run/cycle route tracking |
| Push Notifications | `expo-notifications` | Workout reminders, achievement alerts |
| Camera | `expo-camera` | Progress photos, barcode scanner (supplements) |
| Haptics | `expo-haptics` | Feedback on set completion, achievement unlock |
| Biometrics | `expo-local-authentication` | App lock, secure profile access |

## 6. Backend Integration

- **API base URL**: `https://api.fitpulse.app/v1`
- **Auth method**: JWT (access token 15min, refresh token 7d)
- **Real-time**: WebSocket for live workout leaderboards during challenges
- **Offline support**: Queue actions when offline, sync on reconnect
- **Endpoints**:
  - `POST /auth/login`, `POST /auth/register`, `POST /auth/refresh`
  - `GET /workouts`, `POST /workouts`, `GET /workouts/:id`
  - `GET /exercises`, `GET /exercises/:id`
  - `GET /user/stats`, `GET /user/progress`
  - `GET /challenges`, `POST /challenges/:id/join`
  - `GET /social/friends`, `GET /social/leaderboard`

## 7. Design System

### 7.1 Colors
- Primary: #FF6B35 (energetic orange)
- Secondary: #1A1A2E (deep navy)
- Background: #F8F9FA (light gray)
- Surface: #FFFFFF (white cards)
- Success: #28A745 (green)
- Error: #DC3545 (red)
- Text primary: #1A1A2E
- Text secondary: #6C757D

### 7.2 Typography
- Heading: Inter, weights 600/700
- Body: Inter, weight 400
- Data/Numbers: SF Mono / Roboto Mono, tabular-nums

### 7.3 Spacing
- Base unit: 8px
- Screen padding: 16px horizontal
- Card padding: 16px
- Section gap: 24px
- Bottom tab height: 64px + safe area

### 7.4 Components
- **Activity Ring**: Circular progress, 3 rings (move/calories, exercise, stand), animates on load
- **Workout Card**: Image thumbnail, title, duration, calories, date
- **Set Logger**: Exercise name, weight input, reps input, checkbox per set, auto-timer
- **Streak Flame**: Animated flame icon with day counter
- **Achievement Badge**: Locked/unlocked states, unlock animation (scale + confetti)

## 8. Key Interactions

### 8.1 Workout Flow
1. User taps "Start Workout"
2. Exercise picker modal opens (searchable, filter by muscle group)
3. User selects exercises, taps "Begin"
4. Full-screen workout mode:
   - Current exercise name + demonstration GIF
   - Set counter: "Set 2 of 4"
   - Weight input (kg/lb toggle) + reps input
   - Rest timer: auto-start 60s between sets, editable
   - Next/Previous exercise buttons
   - Finish workout button (swipe to confirm)
5. Post-workout summary: total volume, PRs achieved, calories, share button

### 8.2 Progress Photo Flow
1. Camera opens with overlay grid (front/side/back pose guides)
2. User takes photo, can retake or accept
3. Photo saved locally, auto-synced to cloud
4. Side-by-side comparison view: select two dates, swipe to compare

### 8.3 Social Challenge Flow
1. User browses active challenges
2. Joins challenge, invite friends via link
3. Live leaderboard updates via WebSocket
4. Push notification when overtaken or challenge ends

## 9. Tech Stack

- **Framework**: React Native 0.73 + Expo SDK 50
- **Navigation**: Expo Router (file-based routing)
- **Styling**: NativeWind (Tailwind for RN) + StyleSheet for complex animations
- **State**: Zustand + React Query
- **Auth**: Expo Auth Session + JWT
- **Charts**: React Native Chart Kit
- **Animations**: React Native Reanimated 3
- **Storage**: AsyncStorage + SecureStore
- **Backend**: Supabase (PostgreSQL + Auth + Realtime)
- **Deployment**: EAS Build + App Store / Play Store

## 10. Responsive / Platform Differences

- **iOS**: Follow Human Interface Guidelines, use SF Symbols, respect safe areas
- **Android**: Follow Material Design 3, use system back button, adaptive icons
- **Tablet**: Two-column layout for workout history, larger charts, split-view for exercise library
- **Dark mode**: Full dark theme support, system-aware toggle

## 11. Performance Requirements

- App launch: <2s cold start
- Workout screen load: <500ms
- Chart rendering: <100ms for 90 days of data
- GPS tracking: 1Hz update rate, <5m accuracy
- Bundle size: <50MB (iOS), <30MB (Android)

---

## 生成的提示词（中文）

你是一位资深移动应用开发者。构建一个跨平台健身追踪应用。

## 1. 应用概述

- **应用名称**: FitPulse
- **平台**: iOS 和 Android
- **框架**: React Native 0.73 + Expo SDK 50
- **应用类别**: 健康与健身
- **核心目的**: 帮助用户追踪锻炼、监测健康指标，并通过 AI 驱动的洞察实现健身目标
- **目标用户**: 18-45 岁健身爱好者、健身房常客、跑步者、居家锻炼者

## 2. 页面

| 页面 | 目的 | 关键 UI |
|------|------|--------|
| 引导页 | 用户初始化 | 目标选择、健身水平、偏好设置 |
| 首页/仪表盘 | 每日概览 | 今日锻炼、活动圆环、连续打卡 |
| 锻炼 | 运动追踪 | 计时器、组数/次数计数、休息计时、动作列表 |
| 历史 | 过往锻炼 | 日历视图、锻炼列表、统计摘要 |
| 进度 | 长期趋势 | 图表（体重、力量、耐力）、照片对比 |
| 个人资料 | 用户设置 | 目标、偏好、连接设备、订阅 |
| 社交 | 社区 | 好友列表、排行榜、挑战、分享锻炼 |

## 3. 导航

- **结构**: 底部标签导航（5 个标签：首页、锻炼、历史、社交、个人资料）
- **栈页面**: 引导页 -> 主标签页、锻炼详情、动作库、设置
- **深度链接**: `fitpulse://workout/123`, `fitpulse://challenge/abc`
- **模态框**: 动作选择器、休息计时浮层、分享面板

## 4. 状态管理

- **全局状态**: Zustand（用户资料、锻炼数据、偏好设置）
- **本地状态**: useState/useReducer（表单输入、UI 切换）
- **持久化**: AsyncStorage（认证令牌、用户偏好）、SecureStore（凭证）
- **缓存**: React Query（服务器数据、锻炼历史）
- **后台任务**: expo-background-fetch（应用关闭时同步健康数据）

## 5. 原生功能

| 功能 | 实现方式 | 目的 |
|------|---------|------|
| HealthKit / Google Fit | `expo-health-connect` | 同步步数、心率、卡路里 |
| GPS 追踪 | `expo-location` | 跑步/骑行路线追踪 |
| 推送通知 | `expo-notifications` | 锻炼提醒、成就提醒 |
| 相机 | `expo-camera` | 进度照片、条形码扫描（补剂） |
| 触觉反馈 | `expo-haptics` | 完成一组时的反馈、成就解锁 |
| 生物识别 | `expo-local-authentication` | 应用锁、安全资料访问 |

## 6. 后端集成

- **API 基础地址**: `https://api.fitpulse.app/v1`
- **认证方式**: JWT（访问令牌 15 分钟，刷新令牌 7 天）
- **实时通信**: WebSocket 用于挑战期间的实时锻炼排行榜
- **离线支持**: 离线时排队操作，重新连接后同步
- **接口端点**:
  - `POST /auth/login`, `POST /auth/register`, `POST /auth/refresh`
  - `GET /workouts`, `POST /workouts`, `GET /workouts/:id`
  - `GET /exercises`, `GET /exercises/:id`
  - `GET /user/stats`, `GET /user/progress`
  - `GET /challenges`, `POST /challenges/:id/join`
  - `GET /social/friends`, `GET /social/leaderboard`

## 7. 设计系统

### 7.1 色彩
- 主色: #FF6B35（活力橙）
- 次要: #1A1A2E（深海蓝）
- 背景: #F8F9FA（浅灰）
- 表面: #FFFFFF（白色卡片）
- 成功: #28A745（绿色）
- 错误: #DC3545（红色）
- 文字主色: #1A1A2E
- 文字次要: #6C757D

### 7.2 字体
- 标题: Inter, 字重 600/700
- 正文: Inter, 字重 400
- 数据/数字: SF Mono / Roboto Mono, 等宽数字

### 7.3 间距
- 基础单位: 8px
- 屏幕内边距: 16px 水平
- 卡片内边距: 16px
- 区块间距: 24px
- 底部标签高度: 64px + 安全区域

### 7.4 组件
- **活动圆环**: 圆形进度，3 个圆环（活动/卡路里、锻炼、站立），加载时动画
- **锻炼卡片**: 图片缩略图、标题、时长、卡路里、日期
- **组数记录器**: 动作名称、重量输入、次数输入、每组复选框、自动计时
- **连续打卡火焰**: 带天数计数器的动画火焰图标
- **成就徽章**: 锁定/解锁状态，解锁动画（缩放 + 彩带）

## 8. 关键交互流程

### 8.1 锻炼流程
1. 用户点击"开始锻炼"
2. 动作选择器模态框打开（可搜索，按肌肉群筛选）
3. 用户选择动作，点击"开始"
4. 全屏锻炼模式：
   - 当前动作名称 + 演示 GIF
   - 组数计数器: "第 2 组，共 4 组"
   - 重量输入（kg/lb 切换）+ 次数输入
   - 休息计时器：组间自动开始 60 秒，可编辑
   - 下一个/上一个动作按钮
   - 完成锻炼按钮（滑动确认）
5. 锻炼后总结：总容量、新纪录、卡路里、分享按钮

### 8.2 进度照片流程
1. 相机打开，带有覆盖网格（正面/侧面/背面姿势引导）
2. 用户拍照，可重拍或确认
3. 照片本地保存，自动同步到云端
4. 并排对比视图：选择两个日期，滑动对比

### 8.3 社交挑战流程
1. 用户浏览进行中的挑战
2. 加入挑战，通过链接邀请好友
3. 通过 WebSocket 实时更新排行榜
4. 被超越或挑战结束时推送通知

## 9. 技术栈

- **框架**: React Native 0.73 + Expo SDK 50
- **导航**: Expo Router（基于文件的路由）
- **样式**: NativeWind（RN 版 Tailwind）+ StyleSheet 用于复杂动画
- **状态**: Zustand + React Query
- **认证**: Expo Auth Session + JWT
- **图表**: React Native Chart Kit
- **动画**: React Native Reanimated 3
- **存储**: AsyncStorage + SecureStore
- **后端**: Supabase（PostgreSQL + 认证 + 实时）
- **部署**: EAS Build + App Store / Play Store

## 10. 响应式 / 平台差异

- **iOS**: 遵循人机界面指南，使用 SF Symbols，尊重安全区域
- **Android**: 遵循 Material Design 3，使用系统返回按钮，自适应图标
- **平板**: 锻炼历史双栏布局、更大图表、动作库分屏视图
- **深色模式**: 完整深色主题支持，跟随系统或手动切换

## 11. 性能要求

- 应用启动: 冷启动 <2 秒
- 锻炼页面加载: <500 毫秒
- 图表渲染: 90 天数据 <100 毫秒
- GPS 追踪: 1Hz 更新率，<5 米精度
- 包体积: iOS <50MB，Android <30MB
