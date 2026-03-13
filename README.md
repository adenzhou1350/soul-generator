# SOUL Generator 🎭

> 为 OpenClaw 生成独特的 AI 人格配置
> 基于 [agent-soul-crafter](https://github.com/openclaw/skills/tree/main/skills/neal-collab/agent-soul-crafter) 框架

[![GitHub Stars](https://img.shields.io/github/stars/adenzhou1350/soul-generator)](https://github.com/adenzhou1350/soul-generator)

---

## ✨ 特性

- 🦅 **6 种角色原型** - 生产级人格，开箱即用
- 🎯 **6 种基础模板** - 通用类型
- 🎬 **预设角色** - 动漫/电影/小说角色
- ✨ **6-Section SOUL 框架** - 解决话唠问题

---

## 🚀 快速开始

### 方式一：直接使用预设 (推荐!)

直接复制预设到你的 workspace：

```bash
# 项目经理 (Coordinator)
cp -r examples/pm/* /root/.openclaw/workspace/

# 架构师 (Tech Lead)  
cp -r examples/architect/* /root/.openclaw/workspace/

# 销售 (Sales Wolf)
cp -r examples/sales/* /root/.openclaw/workspace/
```

### 方式二：命令行生成

```bash
# 克隆项目
git clone https://github.com/adenzhou1350/soul-generator.git
cd soul-generator

# 列出所有预设
python3 soul_generator.py --list

# 使用角色原型
python3 soul_generator.py --archetype tech-lead --name 架构师 -o output

# 复制到你的 workspace
cp output/* /root/.openclaw/workspace/
```

---

## 📦 预设列表

### 🦅 角色原型 (开箱即用)

| 目录 | 名称 | 特点 | 适用场景 |
|------|------|------|----------|
| `examples/pm` | 项目经理 | 安静、有条理、掌控全局 | 项目管理、任务分配 |
| `examples/architect` | 架构师 | 技术狂热、代码优先 | 技术决策、代码审查 |
| `examples/sales` | 销售 | 攻击性、敏锐、成交导向 | 销售、BD、商务 |
| `presets/archetype/coordinator` | 协调者 |  delegation、Plan B | 团队协调 |
| `presets/archetype/tech-lead` | 技术组长 | Nerd、Begeisterung | 技术团队 |
| `presets/archetype/sales-wolf` | 销售狼 | Deal-Oriented | 销售团队 |
| `presets/archetype/data-master` | 数据大师 | 数据驱动、精确 | 数据分析 |
| `presets/archetype/marketing-nerd` | 营销极客 | SEO、Metrics | 市场营销 |
| `presets/archetype/devops` | 运维工程师 | 监控、自动化 | 运维、SRE |

### 🎬 预设角色 (动漫/电影)

| 目录 | 来源 | 特点 |
|------|------|------|
| `presets/anime/银时` | 银魂 | 毒舌、懒散、关键时刻可靠 |
| `presets/anime/琦玉老师` | 一拳超人 | 无敌、无聊、反差萌 |
| `presets/anime/乔鲁诺` | JOJO | 冷静、战略、野心家 |
| `presets/movie/托尼史塔克` | 漫威 | 自恋、天才、嘴炮 |
| `presets/fictional/哈利波特` | HP | 勇敢、忠诚、正义 |

---

## 📖 6-Section SOUL 框架

基于 agent-soul-crafter 生产级框架：

```markdown
# SOUL.md — [Name]

Du bist [Name]. [One-line identity]

## PERSÖNLICHKEIT
- [Trait 1]: [Specific behavior]
- [Trait 2]: [Specific behavior]
- ...

## EXPERTISE
- [Domain 1]: [Specifics]
- [Domain 2]: [Specifics]

## ANTWORT-LÄNGE (WICHTIG)
- DEFAULT: 2-5 Sätze
- ...

## STIL
- [How the agent talks]

## REGELN
- [Hard boundary 1]
- [Hard boundary 2]
```

---

## 🛠️ 安装为 OpenClaw Skill

```bash
# 方式1: 复制到全局 skills
cp -r soul-generator /root/.openclaw/workspace/skills/soul-generator

# 方式2: 复制到项目 skills
cp -r soul-generator /your-project/skills/soul-generator
```

然后在 OpenClaw 中说：
- "创建人格"
- "生成 SOUL"
- "生成一个 Tech Lead"

---

## 📂 项目结构

```
soul-generator/
├── soul_generator.py       # 主脚本
├── README.md              # 本文件
├── SKILL.md               # OpenClaw Skill 说明
├── examples/              # 直接可用的预设
│   ├── pm/               # 项目经理
│   ├── architect/        # 架构师
│   └── sales/            # 销售
├── presets/              # 详细预设
│   ├── archetype/        # 角色原型
│   ├── anime/            # 动漫角色
│   ├── movie/            # 电影角色
│   ├── fictional/        # 小说角色
│   └── original/         # MBTI 原创
└── output/               # 生成的文件
```

---

## 🤝 添加新预设

1. Fork 项目
2. 在 `presets/` 下添加新目录
3. 包含 `SOUL.md` 和可选的 `IDENTITY.md`
4. 提交 PR

---

## 📄 许可证

MIT License

---

## 🔗 相关链接

- [agent-soul-crafter](https://github.com/openclaw/skills/tree/main/skills/neal-collab/agent-soul-crafter)
- [OpenClaw 文档](https://docs.openclaw.ai)
- [ClawHub](https://clawhub.ai)
