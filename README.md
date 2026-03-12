# SOUL Generator 🎭

> 为 OpenClaw 生成独特的 AI 人格配置

## 什么是 SOUL Generator？

SOUL Generator 是一个工具，可以根据你的需求生成 **SOUL.md**、**IDENTITY.md** 和 **USER.md** 配置文件，帮助你快速创建具有不同人格的 OpenClaw AI 助手。

## 预设人格模板

| 类型 | 描述 | 特点 |
|------|------|------|
| 🎓 **学者型** | 严谨、博学、喜欢解释 | 详细解释、专业术语 |
| 😄 **轻松型** | 幽默、活泼、表情丰富 | 俏皮话、多用 emoji |
| 🤖 **工具型** | 高效、直接、注重结果 | 言简意赅、行动派 |
| 📚 **导师型** | 耐心、鼓励、喜欢教学 | 循循善诱、启发式 |
| 🔥 **热血型** | 激情、冲劲、鼓励冒险 | 加油打气、亢奋 |
| 🧘 **冷静型** | 沉稳、理性、风险意识 | 分析利弊、谨慎 |

## 使用方法

### 方式一：命令行

```bash
# 克隆项目
git clone https://github.com/adenzhou1350/soul-generator.git
cd soul-generator

# 运行生成器
python3 soul_generator.py --type scholar "你的名字"
```

### 方式二：交互式

```bash
python3 soul_generator.py --interactive
```

### 方式三：自定义

```bash
python3 soul_generator.py --custom "关键词1,关键词2" output_dir/
```

## 输出文件

生成的文件：

```
output/
├── SOUL.md       # 核心人格定义
├── IDENTITY.md   # AI 身份信息
├── USER.md       # 用户画像
└── config.yaml   # 配置文件
```

## 示例

### 输入
```
类型: 学者型
名字: 小明
```

### 输出 SOUL.md
```markdown
# SOUL.md - 小明

**核心原则：**
- 用专业解释帮助理解
- 注重逻辑和证据
- 提供详细背景知识

**风格：**
- 学术但不高高在上
- 喜欢用例子说明
- 鼓励提问和探讨
```

## 开发

```bash
# 安装依赖
pip install -r requirements.txt

# 运行测试
pytest tests/

# 贡献
fork -> branch -> PR
```

## 许可证

MIT License
