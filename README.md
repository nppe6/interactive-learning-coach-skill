# Interactive Learning Coach Skill

一个交互式学习教练 Skill 模板。当前仓库按 Codex Skill 结构组织，但教学方法、提示词结构和参考模板也可以迁移到 Claude Code、ChatGPT、自定义 Agent 或其他支持技能/系统提示的环境。

它融合 ChatGPT Study Mode 的启发式教学、Gemini Guided Learning 的测验与学习卡片能力，并加入学习路线图、四步教学设计、学习文档、复习计划和项目实战迁移。

## 核心目标

`interactive-learning-coach` 不只是讲解知识点，而是把学习过程组织成一个可持续推进的学习系统：
- 开始前生成鸟瞰版学习路线图
- 每个知识点按四步教学设计备课
- 学习中通过提问、提示、测验检查理解
- 学完后沉淀为可复习的 Markdown 文档
- 记录课程进度、薄弱点和下次续学位置
- 支持回访复习、二刷重讲和补充讲解
- 定期生成复习任务、错因修复和迁移练习
- 模块结束后设计实战项目

## 核心能力

### 1. 鸟瞰版学习路线图
学习课程、开源项目或大型主题前，先生成类似“学期教学计划”的路线图，包含学习目标、章节大纲、主要知识点、复习点、练习点和项目检查点。

初版路线图不追求一次性完整，而是先给出方向，再随着学习深入逐章细化。

### 2. 四步教学设计内核
每个主要知识点都会按照四步设计：
1. 心智接口设计：探测前概念，制造认知冲突，说明真实用途。
2. 最小可行理解：提炼不可省略的一点，给出核心隐喻，说明知识地图位置。
3. 练习阶梯设计：识别常见卡点，设计防错练习，提供多种变式。
4. 迁移桥梁：从例子迁移到一类问题，使用对比案例，组合旧知识解决新问题。

### 3. 学习文档沉淀
重要课程、章节、知识点或开源项目阅读会沉淀为 Markdown 文档，默认目录为：
```text
learning-notes/
```
示例文件名：
```text
learning-notes/react-learning-roadmap.md
learning-notes/react-hooks-useeffect.md
learning-notes/vue-source-code-roadmap.md
learning-notes/open-source-project-auth-flow.md
```

### 4. 复习与实战
每个学习文档都会带有复习计划，例如 Now、Day 1、Day 3、Day 7、Day 14-30。复习重点不是重读，而是回忆、解释、错因修复和迁移应用。

模块学习完成后，Skill 会生成 Guided drill、Mini project 或 Capstone project，把课程例题或开源项目模式迁移成可实践任务。

## 目录结构

```text
.
├── LICENSE
├── README.md
└── skills/
    └── interactive-learning-coach/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        └── references/
            ├── learning-artifacts.md
            ├── product-kernels.md
            └── session-patterns.md
```

## 安装

将 Skill 目录复制到 Codex 的 skills 目录。

Windows：
```powershell
Copy-Item -Recurse .\skills\interactive-learning-coach $env:USERPROFILE\.codex\skills\
```
macOS / Linux：
```bash
cp -R ./skills/interactive-learning-coach ~/.codex/skills/
```
安装后，在新会话中使用 `$interactive-learning-coach` 调用。

其他 Agent 环境可以直接复用 `skills/interactive-learning-coach/SKILL.md` 的主体提示词，并按目标平台改写安装目录和元数据文件。

## 使用示例

```text
使用 $interactive-learning-coach 带我学习线性代数。我基础一般，请先给我鸟瞰版学习路线，再从第一章开始互动教学。
```
```text
使用 $interactive-learning-coach 带我学习这个开源项目。请先分析项目结构，生成学习路线图，然后按模块讲解，并为每个模块设计实战任务。
```
```text
使用 $interactive-learning-coach 根据课程 PDF 生成学习路线、章节笔记、Quiz Cards、Flashcards 和复习计划。
```


## 许可证

本项目使用 Apache License 2.0，详见 [LICENSE](./LICENSE)。