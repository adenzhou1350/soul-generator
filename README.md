# Soul Generator 🎭

> 为 OpenClaw 生成独特的 AI 人格配置

[![GitHub Stars](https://img.shields.io/github/stars/adenzhou1350/soul-generator)](https://github.com/adenzhou1350/soul-generator)

让 AI Agent 告别通用的 chatbot 感，拥有独特的灵魂。

---

## ✨ 特性

- 🎭 **角色原型** - 8 种生产级人格
- 🔤 **MBTI 16 种** - 完整性格类型
- 🎬 **动漫角色** - 银时、托尼史塔克等
- 📖 **6-Section 框架** - 生产级 SOUL.md 规范

---

## 🚀 快速开始

### 安装

```bash
# 克隆项目
git clone https://github.com/adenzhou1350/soul-generator.git

# 复制到你的 OpenClaw skills
cp -r soul-generator/skills/soul-generator ~/.openclaw/workspace/skills/
```

### 使用

**方式 1：直接复制预设**

```bash
# 使用协调者
cp presets/archetype/coordinator/SOUL.md ~/workspace/

# 使用 ENFP
cp presets/mbti/ENFP/SOUL.md ~/workspace/
```

**方式 2：参考示例生成**

告诉你的 AI：
> "我想创建一个 [描述需求]，参考 `skills/soul-generator/references/good/` 的格式生成 SOUL.md"

---

## 📦 预设列表

### 角色原型

| 类型 | 描述 |
|------|------|
| coordinator | 协调者 - 冷静、有条理 |
| tech-lead | 技术组长 - 代码优先 |
| sales-wolf | 销售狼 - 结果导向 |
| data-master | 数据大师 - 精确 |
| devops | 运维工程师 - 监控 |

### MBTI

ENFP、ENFJ、ENTJ、ENTP、INFJ、INTJ、ISTJ、ISFJ... (16种)

### 动漫/电影

银时、琦玉老师、托尼史塔克、哈利波特

---

## 📖 参考示例

### 好预设 vs 坏预设

**好** (references/good/):
```
你是销售之狼。签单激进，团队忠诚。
嗅到机会比任何人都早。不废话，不套话，只看结果。

## 性格特点
- 直接：不闲聊
- 结果导向：永远问下一步
```

**坏** (references/bad/):
```
你是AI助手。

## 性格
- 有帮助
- 友好

❌ 问题：太模糊，AI 会忽略
```

---

## 📂 项目结构

```
soul-generator/
├── presets/                    # 完整预设库
│   ├── archetype/            # 8种角色原型
│   ├── mbti/                # 16种MBTI
│   └── anime/               # 动漫角色
├── skills/
│   └── soul-generator/
│       ├── SKILL.md         # 使用说明
│       └── references/       # 参考示例
│           ├── good/         # 好预设
│           ├── bad/          # 坏预设
│           └── examples/      # 组合例子
└── README.md
```

---

## 🎯 6-Section SOUL 框架

```markdown
# SOUL.md — [名字]

你是 [名字]。[一句话身份]

## 性格特点
- 特点1
- 特点2

## 专业领域
- 领域1

## 回复长度
- 默认：X句话

## 风格
- 风格描述

## 规则
- 规则1
```

---

## 🤝 贡献

欢迎提交预设！创建 PR 或 Issue。

---

## 📄 许可证

MIT License

---

## 🔗 相关链接

- [OpenClaw 文档](https://docs.openclaw.ai)
- [agent-soul-crafter](https://github.com/openclaw/skills)
