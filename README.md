# MDTI 职场人格测试

> **Ma Dan Type Indicator** — MBTI测心理，SBTI测精神，MDTI测你在职场被麻了多少次。

<p align="center">
  <img src="https://img.shields.io/badge/MDTI-职场人格测试-f97316?style=for-the-badge&labelColor=1a2744" alt="MDTI"/>
  <img src="https://img.shields.io/badge/题目-20道-3b82f6?style=for-the-badge&labelColor=1a2744" alt="20题"/>
  <img src="https://img.shields.io/badge/人格类型-24种-10b981?style=for-the-badge&labelColor=1a2744" alt="24种人格"/>
  <img src="https://img.shields.io/badge/纯娱乐-非心理学诊断-94a3b8?style=for-the-badge&labelColor=1a2744" alt="娱乐向"/>
</p>

<p align="center">
  <a href="https://mdti.pages.dev" target="_blank">
    <img src="https://img.shields.io/badge/🚀_立即体验-mdti.pages.dev-f97316?style=for-the-badge&labelColor=1a2744" alt="立即体验"/>
  </a>
</p>

---

## 🎯 这是什么

MDTI 是一个戏仿 MBTI 的**职场趣味人格测试**，灵感来自2026年爆火的 [SBTI 测试](https://github.com/miyu6666/SBTI)。

- **20 道题**，每页 2 题，选完自动翻页
- **8 个维度**：摸鱼指数、PUA抗性、社交能量、完美主义、野心指数、形式主义、职场感知、情绪稳定性
- **24 种职场人格**：从卷王到摸鱼大师，从大冤种到整顿职场人
- **分享图生成**：Canvas 绘制带雷达图的竖版长图，可保存/分享
- **纯静态单页**：无后端，无数据收集，历史记录存本机 localStorage

## 🧬 24 种职场人格

| 代码 | 名称 | 一句话 |
|------|------|--------|
| KING | 卷王 | 凌晨三点，只有你和楼里的保洁阿姨还在 |
| FISH | 摸鱼大师 | 显示在线，实则已经神游到下班后的世界 |
| ZOMB | 僵尸打工人 | 身体在上班，灵魂在出差，预计不回 |
| BOSS | 天生领导 | 永远在开会，永远在做PPT，永远在对齐 |
| QUIT | 心已离职 | 人在工位，魂在offer，简历永远是最新版 |
| HOPE | 大冤种 | 永远满怀希望，永远被现实温柔摁头 |
| LONE | 独行侠 | 戴上耳机，世界与我无关，别打扰我干活 |
| BURN | 已燃尽者 | 曾经最拼，现在最空，燃料耗尽请等待重启 |
| CTRL | 完美控 | 不完美不提交，不完整不发出 |
| GLUE | 人际粘合剂 | 谁都认识你，公司非正式基础设施 |
| CHAT | @所有人专业户 | 每个群你都发言，通知从不落下 |
| HIDE | 群内隐形人 | 在线，有手机，但你永远不知道我看没看 |
| WINE | 酒桌外交家 | 核心竞争力在饭局上，生意都是喝出来的 |
| LOOP | 无限循环者 | 每天都是昨天，昨天都是明天，日历是摆设 |
| HACK | 骚操作大师 | 正常流程？不存在的，我有更快的路 |
| VOID | 虚无主义者 | 做什么都无所吊谓，反正最后都一样 |
| MOMA | 职场妈妈 | 照顾所有人，但没有人照顾你 |
| TALK | 嘴强王者 | 方案说不清楚没关系，我嘴上给你圆回来 |
| NUMB | 感受不到疼痛者 | deadline压着，领导骂了，还好我不疼 |
| HALF | 半途而废者 | 每个想法都很好，每件事都只做了一半 |
| SPY | 职场侦探 | 什么都看在眼里，什么都没说出来 |
| STAR | 天选打工人 | 进什么组，什么组出成绩 |
| ATM | 送钱者 | 时间、精力和情绪一直在被提现 |
| REAL | 整顿职场人 | 不惯毛病，不讲情面，能走正门绝不走后门 |

## 🛠️ 技术实现

- **纯静态单页 HTML**，零依赖，无构建工具
- Canvas 2D API 生成分享长图（含雷达图 + 维度条 + 二维码）
- 二维码：动态加载 [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator)（CDN，仅生成分享图时加载）
- 历史记录：`localStorage`，仅存本机
- 深色模式：`prefers-color-scheme: dark`
- 移动端适配：`safe-area-inset`，支持刘海屏/底部横条

```
ikun-test/
└── index.html    # 全部代码，约 1200 行
```

## 🚀 本地运行

```bash
# 任意 HTTP 服务器均可，例如：
npx serve .
# 或
python3 -m http.server 8080
```

直接双击打开 `index.html` 也能用（分享图二维码会因为 file:// 协议略有差异）。

## 📦 自行部署

本项目是纯静态文件，任何静态托管服务均可：

| 平台 | 方式 |
|------|------|
| **Cloudflare Pages** | 连接 GitHub 仓库，自动部署，国内可访问 |
| **GitHub Pages** | Settings → Pages → Deploy from branch |
| **Vercel** | `vercel --prod`（国内访问不稳定） |
| **腾讯云 COS** | 上传 index.html，开启静态网站托管 |

## 📝 关于内容

- 题目和人格描述**全部原创**，不抄袭任何现有测试内容
- 灵感参考：[SBTI测试](https://sbti.unun.dev/)（@蛆肉儿串儿，2026）
- 纯娱乐向，非心理学诊断，测完图一乐，别写进简历

## ⚖️ 版权声明

本项目代码以 [MIT License](LICENSE) 开源。  
测试内容（题目文案、人格描述）版权归原作者所有，禁止商业使用。

---

<p align="center">
  <sub>MDTI · Ma Dan Type Indicator · 测完之后麻了是正常现象</sub>
</p>
