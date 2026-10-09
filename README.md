# Soul Generator · 把工作习惯写进 Agent

把「希望助手怎样说话、怎样做事」整理成一份可编辑的 `SOUL.md`。

这是给 Agent 使用的 **Skill 和人格模板集合**。生成工作由你使用的模型完成；仓库本身没有独立的生成服务，也不需要填写 API key。

[看输入与输出](#先看一个例子) · [安装](#安装) · [预设目录](skills/soul-generator/presets) · [作者的项目与教学](https://adenzhou1350.github.io/)

## 先看一个例子

给已加载这个 Skill 的助手发一段描述：

```text
帮我生成一份 SOUL.md：
我想要一个帮我整理研究笔记的助手。
说话直接，但别替我下结论；先列证据，再讲判断。
遇到不确定的地方要说清楚，不要编造经历。
先把草稿给我看，不要覆盖现有配置。
```

生成的草稿会包含性格、表达方式、回复规则和边界。默认交付位置见 [Skill 说明](skills/soul-generator/SKILL.md)，通常为 `~/.openclaw/workspace/soul/[名字]/SOUL.md`；生成后需要你检查并决定是否启用。

例如，上面的要求可以整理为下面这样的片段；这是格式示意，实际结果取决于你使用的模型：

```markdown
## 回复规则
- 整理研究笔记时，分别列出材料中的事实、你的推断和待核对问题。
- 引用结论时给出对应材料；材料没有的信息明确写“未提供”。

## 边界
- 不为增强角色感而编造个人经历。
- 修改配置前先展示草稿，由用户决定是否启用。
```

启用前，用同一份笔记分别测试原配置和新配置，检查助手有没有按这些规则回答。`SOUL.md` 是行为提示，不能替代宿主的工具权限或执行控制。

也可以先读一个现成模板：[技术助手](skills/soul-generator/presets/archetype/tech-lead/SOUL.md) · [协调者](skills/soul-generator/presets/archetype/coordinator/SOUL.md) · [INTP](skills/soul-generator/presets/mbti/INTP/SOUL.md)。

## 安装

下面是 Bash 命令（Linux、macOS 或 WSL）。先克隆仓库：

```bash
git clone https://github.com/adenzhou1350/soul-generator.git
cd soul-generator
```

选择你的工具，把 **包含 SKILL.md 的子目录** 复制进去：

```bash
# OpenClaw
mkdir -p ~/.openclaw/workspace/skills
cp -r skills/soul-generator ~/.openclaw/workspace/skills/
```

```bash
# Claude Code，安装到当前项目
mkdir -p .claude/skills
cp -r skills/soul-generator .claude/skills/
```

Windows 原生环境可手动复制同一目录。已有同名 Skill 时，先备份旧版本。安装后按所用工具的方式重新加载 Skill，再发送上面的描述。

## 三种用法

| 方式 | 你提供什么 | 需要什么 |
| --- | --- | --- |
| 自定义 | 用途、语气、工作习惯、边界 | 模型读取 Skill 的能力 |
| 类型预设 | MBTI / SBTI 类型，加上自己的描述 | [预设模板](skills/soul-generator/presets) |
| 参考人物 | 人名、想参考的思考或表达方式 | 宿主提供搜索工具，并保留来源 |

人物模式是基于公开资料的风格整理，输出仍是模型生成的草稿。MBTI / SBTI 在这里用作写作提示，不作为人格测评。没有搜索工具时，请提供资料，或直接用自定义模式。

现有模板包含 16 个 MBTI、16 个 SBTI、3 个角色原型，以及动漫、电影和虚构人物。完整流程与格式见 [SKILL.md](skills/soul-generator/SKILL.md)。

## 改成自己的版本

最有用的修改往往是具体行为：比如「先给最小可运行示例」「不确定时列出缺失信息」，而不只是增加形容词。

欢迎提交模板或使用反馈。新模板放在 `skills/soul-generator/presets/<类别>/<名字>/SOUL.md`，附一个输入示例和预期行为即可。请使用虚构或已获允许的信息，避免把个人隐私或凭据写入配置。

## 相关仓库怎么选

| 你想做的事 | 从哪里开始 |
| --- | --- |
| 从一句描述生成新的行为配置 | 当前仓库：Soul Generator |
| 直接选现成人格，配置 OpenClaw 工作区 | [openclaw-starter](https://github.com/adenzhou1350/openclaw-starter) |
| 阅读资源检查、提醒、备份等独立例子 | [openclaw-examples](https://github.com/adenzhou1350/openclaw-examples) |
| 组合天气早报、提醒与工作区复盘脚本 | [openclaw-automation](https://github.com/adenzhou1350/openclaw-automation) |

更多 Agent 项目与实战笔记见 [个人网站](https://adenzhou1350.github.io/projects/) 和 [教学区](https://adenzhou1350.github.io/learn/)。

[MIT License](LICENSE)
