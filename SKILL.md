# soul-generator

> 为 OpenClaw 生成定制化 AI 人格

## 描述

使用 soul-generator 为自己或客户创建独特的 AI 人格。

## 触发条件

用户说：
- "创建人格"
- "生成 SOUL"
- "定制 AI 人格"
- "让我换个性格"
- "生成一个 Tech Lead"

## 使用方法

### 1. 列出所有预设

```bash
cd /root/.openclaw/workspace/skills/soul-generator
python3 soul_generator.py --list
```

### 2. 使用角色原型

```bash
python3 soul_generator.py --archetype coordinator --name 项目经理
python3 soul_generator.py --archetype tech-lead --name 架构师
python3 soul_generator.py --archetype sales-wolf --name 销售
```

### 3. 直接复制预设

```bash
# 协调者
cp presets/archetype/coordinator/SOUL.md /root/.openclaw/workspace/SOUL.md

# 技术组长
cp presets/archetype/tech-lead/SOUL.md /root/.openclaw/workspace/SOUL.md
```

## 预设列表

### 角色原型

| 参数 | 名称 | 特点 |
|------|------|------|
| `coordinator` | 协调者 | 冷静、有条理、委托型 |
| `tech-lead` | 技术组长 | 技术控、热情、动手派 |
| `sales-wolf` | 销售狼 | 直接、结果导向 |
| `data-master` | 数据大师 | 精确、结构化 |

### 基础模板

| 参数 | 名称 | 特点 |
|------|------|------|
| `scholar` | 学者型 | 严谨、博学 |
| `casual` | 轻松型 | 幽默、活泼 |
| `tool` | 工具型 | 高效、直接 |
| `mentor` | 导师型 | 耐心、鼓励 |
| `energetic` | 热血型 | 激情、正能量 |
| `calm` | 冷静型 | 沉稳、理性 |

## 输出文件

```
output/
├── SOUL.md       # 核心人格
├── IDENTITY.md   # 身份信息
└── USER.md       # 用户画像
```

## 应用到 OpenClaw

```bash
cp output/SOUL.md /root/.openclaw/workspace/
cp output/IDENTITY.md /root/.openclaw/workspace/
```

---

**基于**: [agent-soul-crafter](https://github.com/openclaw/skills/tree/main/skills/neal-collab/agent-soul-crafter)
