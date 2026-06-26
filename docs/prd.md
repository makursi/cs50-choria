# PRD: CS50x 2026 个人学习日志仓库

## Problem Statement

用户正在学习 Harvard CS50x 2026（计算机科学导论），需要一个结构清晰的 GitHub 仓库来记录和跟踪个人的完整学习过程，包括课程笔记和所有编程练习的解答代码。

## Solution

建立一个以「周」为组织单位的个人学习日志仓库。每周一个文件夹，内含该周的课程笔记（Markdown）和所有问题集（Problem Set）源代码文件。代码在本地环境编写，通过 Git 逐题提交，形成完整的学习轨迹。

## User Stories

1. 作为一个 CS50 学习者，我希望能按周浏览自己的学习进度，以便快速回顾某周的内容。
2. 作为一个 CS50 学习者，我希望每周末的笔记和代码放在同一个文件夹里，以减少查找成本。
3. 作为一个 CS50 学习者，我希望每道题的解答单独 commit，以便日后追溯解题思路的演变。
4. 作为一个 CS50 学习者，我希望仓库结构简单、不嵌套过深，以便快速定位文件。
5. 作为一个 CS50 学习者，我希望 Less Comfortable 和 More Comfortable 两个难度的题目都能练习并保存。
6. 作为一个 CS50 学习者，我希望笔记用中文写、代码注释用英文写，以兼顾个人阅读效率和专业习惯。
7. 作为一个 CS50 学习者，我希望 commit message 使用英文，以符合开源社区惯例。
8. 作为一个 CS50 学习者，我希望 C 语言的编译产物和 IDE 配置文件不被提交到仓库，以保持仓库整洁。
9. 作为一个 CS50 学习者，我希望最终项目放在独立仓库中，与课程练习仓库分离，以便独立展示。
10. 作为一个 CS50 学习者，我希望 Week 0（Scratch）只存放笔记，不放项目文件或截图。
11. 作为一个 CS50 学习者，我希望能在本地环境（Windows 11）完成所有编程练习，不依赖 cs50.dev 在线环境。
12. 作为一个 CS50 学习者，我希望仓库 README 极简，不做进度追踪和环境记录。

## Implementation Decisions

### 仓库目录结构

根目录下按周创建文件夹，命名格式为 `week-N-topic/`。最终项目另建独立仓库，不出现在本仓库中。

```
cs50x-2026/
  README.md
  .gitignore
  week-0-scratch/
    notes.md
  week-1-c/
    notes.md
    hello.c
    mario-less.c
    mario-more.c
    cash.c
    credit.c
  week-2-arrays/
    notes.md
    ...
  ...
  week-10-cybersecurity/
    notes.md
```

### 每周文件夹内容约定

- `notes.md` — 该周课程笔记（中文）
- 源文件直接放在该周文件夹根下，不额外嵌套 `pset/`、`lab/` 子目录
- 文件命名沿用 CS50 官方分发代码的文件名

### 难度覆盖策略

CS50 大部分问题集分为 Less Comfortable 和 More Comfortable 两个难度。用户两个都做，Less 作为热身，More 作为进阶。

### 开发环境

- 全部代码在本地环境编写和测试，不使用 cs50.dev
- 不安装 check50 / style50 CLI 工具
- 用户自行配置 C 编译器（GCC）、Python、SQLite 等
- 操作系统：Windows 11

### Git 策略

- 一题一 commit，commit message 使用英文
- 不 squash，保留解题过程的完整历史

### 语言约定

| 内容 | 语言 |
|------|------|
| `notes.md` | 中文 |
| 代码注释 | 英文 |
| commit message | 英文 |
| README.md | 中文或英文皆可 |

### .gitignore

忽略以下内容：

- C 编译产物：`*.exe` `*.o` `*.out`
- Python 缓存：`__pycache__/`
- IDE 配置：`.vscode/` `.idea/`

### README.md

仅做简要介绍，不包含进度清单或环境配置说明。

### 最终项目

CS50 Final Project 将在独立 GitHub 仓库中进行，不在本仓库范围内。

## Testing Decisions

本仓库为个人学习日志，不涉及自动化测试。每道题的正确性由用户自行验证（本地运行），不强制使用 check50。

## Out of Scope

- 最终项目（Final Project）—— 独立仓库
- CS50 证书获取 —— 本仓库不追踪证书进度
- GitHub Actions / CI —— 不配置
- check50 / style50 自动评分 —— 不使用
- 多人协作 —— 纯个人仓库
- 讲座视频链接或截图收集
- 中文翻译或双语对照
- Week 0 的 `.sb3` 文件或 Scratch 截图

## Further Notes

- 仓库将在用户本地初始化，通过 Git 管理后推送到 GitHub
- 用户已有 C 语言基础（链表、二叉树等数据结构），C 阶段（Week 1-5）更多是复习性质
- 仓库名称建议：`cs50x-2026`
