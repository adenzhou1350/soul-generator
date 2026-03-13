# Soul Generator

> 为 OpenClaw 生成独特的 AI 人格配置

## 简介

Soul Generator 可以帮助你快速创建具有独特人格的 AI 助手。

基于 [agent-soul-crafter](https://github.com/openclaw/skills/tree/main/skills/neal-collab/agent-soul-crafter) 框架。

## 安装

```bash
# 克隆项目
git clone https://github.com/adenzhou1350/soul-generator.git
cd soul-generator

# 安装为 OpenClaw Skill
cp -r soul-generator /root/.openclaw/workspace/skills/soul-generator
```

## 使用方法

### 命令行

```bash
# 列出所有预设
python3 soul_generator.py --list

# 使用角色原型
python3 soul_generator.py --archetype tech-lead --name 架构师

# 使用基础模板
python3 soul_generator.py --type casual --name 小助手
```

### 直接复制预设

```bash
# 项目经理
cp presets/archetype/coordinator/SOUL.md /root/.openclaw/workspace/SOUL.md

# 架构师
cp presets/archetype/tech-lead/SOUL.md /root/.openclaw/workspace/SOUL.md
```

## 预设列表

### 角色原型 (Archetype)

| 目录 | 名称 | 特点 |
|------|------|------|
| `coordinator` | 协调者 | 冷静、有条理、委托型 |
| `tech-lead` | 技术组长 | 技术控、热情、动手派 |
| `sales-wolf` | 销售狼 | 直接、结果导向 |
| `data-master` | 数据大师 | 精确、结构化 |

### 基础模板

| 目录 | 名称 | 特点 |
|------|------|------|
| `scholar` | 学者型 | 严谨、博学 |
| `casual` | 轻松型 | 幽默、活泼 |
| `tool` | 工具型 | 高效、直接 |
| `mentor` | 导师型 | 耐心、鼓励 |
| `energetic` | 热血型 | 激情、正能量 |
| `calm` | 冷静型 | 沉稳、理性 |

## 输出文件

生成的文件包含：

- `SOUL.md` - 核心人格定义 (6-Section 框架)
- `IDENTITY.md` - AI 身份信息
- `USER.md` - 用户画像

## 6-Section 框架

```markdown
# SOUL.md — [Name]

你是 [Name]。[一句话身份]

## 性格特点
- 特点1
- 特点2

## 专业领域
- 领域1
- 领域2

## 回复长度（重要）
- 默认：X句话
- ...

## 风格
- 风格描述

## 规则
- 规则1
- 规则2
```

## 许可证

MIT License
