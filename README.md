<div align="center">

# Soul Generator 🎭

> *「让 AI 成为另一个你 — 或者你想成为的那个人」*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Compatible-green)](https://openclaw.ai)

<br>

**三种方式生成你的 AI 分身：**

**① 蒸馏名人** — 输入名字，自动上网搜索，生成可运行的思维框架

**② SBTI / MBTI** — 选类型，加你的背景，生成专属配置

**③ 完全自定义** — 用你的语言描述，生成独特人格

[快速开始](#-快速开始) · [效果示例](#-效果示例) · [三种模式详解](#-三种模式) · [预设列表](#-预设列表)

<br>

[![Star History](https://api.star-history.com/svg?repos=adenzhou1350/soul-generator&type=Date)](https://star-history.com/#adenzhou1350/soul-generator&Date)

</div>

---

## 🎯 效果示例

### 蒸馏名人

```
用户      ❯ 帮我蒸馏乔布斯

Soul     ❯ 正在搜索乔布斯的著作、访谈、决策记录...
         构建中...
         已生成乔布斯视角的 SOUL.md
```

### SBTI + 个人背景

```
用户      ❯ 我是 MALO（吗喽），做过独立开发
         讨厌开会，常说"干就完了"
         生成我的 SOUL.md

MALO     ❯ 正在生成...
         已生成你的专属配置
```

### 直接使用预设

```
用户      ❯ 用 BOSS 风格生成 SOUL.md

BOSS     ❯ 已生成。基于领导者原型的配置。
```

---

## 🚀 快速开始

### 安装

**OpenClaw（推荐）**
```bash
# 一键从 GitHub 安装
clawhub install adenzhou1350/soul-generator
```

**手动安装（所有 Agent 通用）**
```bash
git clone https://github.com/adenzhou1350/soul-generator.git
cd soul-generator

# OpenClaw
cp -r skills/soul-generator ~/.openclaw/workspace/skills/

# Claude Code（全局）
cp -r skills/soul-generator ~/.claude/skills/

# Claude Code（项目级）
mkdir -p .claude/skills
cp -r skills/soul-generator .claude/skills/
```

**Claude Code / Claude.ai**
```bash
# 项目级安装
mkdir -p .claude/skills
git clone https://github.com/adenzhou1350/soul-generator.git .claude/skills/soul-generator

# 或全局安装
git clone https://github.com/adenzhou1350/soul-generator.git ~/.claude/skills/soul-generator
```

**其他 Agent（Cursor, Cline, VS Code Copilot 等）**
```bash
# 通常是复制到对应工具的 skills 目录
# 参考各工具的 skills 安装方式
```

### 使用

```
> 帮我蒸馏乔布斯

> 我是 MALO，做过独立开发，讨厌开会
> 生成我的 SOUL.md

> 用 ENTP 风格生成 SOUL.md

> 做一个产品经理的人设，直接、不耐烦、讨厌无效会议
```

---

## 🔥 三种模式

### 模式一：蒸馏名人（自动上网搜索）

输入一个人名，Skill 自动完成：

1. **4路并行搜索** — 著作、访谈、社交媒体、决策记录
2. **心智模型提炼** — 他用什么框架看世界？判断标准是什么？
3. **表达DNA提取** — 口头禅、说话风格、典型句式
4. **生成 SOUL.md** — 组装成可用的配置文件

```
> 帮我蒸馏乔布斯
> 用马斯克的视角分析这个决策
> 做一个张一鸣的思维框架
```

### 模式二：SBTI / MBTI + 个人背景

基于预设人格类型，融合你的个人经历：

```
> 我是 MALO，做过独立开发、创业失败过一次
> 讨厌开会，常说"干就完了"
> 生成我的 SOUL.md
```

预设类型：
- **SBTI**：MALO / BOSS / CTRL / DEAD / 等16型
- **MBTI**：ENFP / INTJ / ENTJ / 等16型

### 模式三：完全自定义描述

用自然语言描述你要生成的人：

```
> 帮我生成一个 AI 人格
> 他：直接、不耐烦、喜欢动手大于动嘴
> 做过：抖音早期员工，创业2次
> 讨厌：无意义会议和废话
```

---

## 📂 输出文件

```
~/.openclaw/workspace/soul/[名字]/SOUL.md
```

**一个文件，包含一切。** Skill 只在生成时调用一次，之后模型直接读 SOUL.md。

---

## 📦 预设列表

### 🔥 SBTI（2026新爆款）

| 类型 | 名称 | 类型 | 名称 |
|------|------|------|------|
| MALO | 吗喽 | POOR | 贫穷者 |
| SEXY | 尤物 | OJBK | 无所谓人 |
| BOSS | 领导者 | OHNO | 哦不人 |
| FUCK | 草者 | MONK | 僧人 |
| CTRL | 拿捏者 | SHIT | 狗屎人 |
| DEAD | 死者 | ATM | 送钱者 |
| ZZZZ | 装死者 | SOLO | 孤儿 |
| GOGO | 行者 | JOKER | 小丑 |

### MBTI（16型）

ENFP · ENFJ · ENTJ · ENTP · INFJ · INTJ · ISTJ · ISFJ · ESFJ · ESFP · ESTJ · ESTP · INFP · ISFP · ISTP

### 角色原型

coordinator · tech-lead · sales-wolf

### 动漫/电影

坂田银时 · 琦玉老师 · 托尼史塔克 · 哈利波特

---

## 🤝 贡献

欢迎提交新预设！

1. 在对应目录下创建目录
2. 添加 `SOUL.md`
3. 提交 PR

---

## 📄 许可证

MIT License
