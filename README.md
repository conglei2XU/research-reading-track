# Weekly Reading & Release Logs

> 用于团队共同维护每周待阅读论文列表、阅读笔记，以及需要持续关注的开源项目和工具 release logs。

This repository is a lightweight shared workspace for maintaining weekly paper reading lists, paper notes, and release logs of open-source projects, tools, models, and datasets that the team needs to track.

---

## 1. 仓库定位

本仓库主要用于团队同步以下内容：

1. 每周需要阅读的论文列表；
2. 成员完成后的论文阅读笔记；
3. 需要持续关注的开源项目、工具、模型或数据集的 release logs；
4. 每周新增或发生变化的重要阅读材料与工具更新记录。

为团队提供一个轻量、可追踪、便于协作更新的阅读与工具动态同步空间。

---

## 2. Latest Updates｜本周更新

本章节用于汇总每周最新更新的阅读清单、阅读笔记和开源项目 release logs。详细内容应写入 `updates/` 目录下对应周次的 Markdown 文件，README 中只保留索引。

### 最近更新(2026-07-21)

| Week                 | Update Summary        | Reading List                 | Release Logs | Notes |
|----------------------|-----------------------|------------------------------|---|---|
| 2026-W01(2026-07-21) | `updates/2026-W02.md` | `weekly-reading/2026-W02.md` | - | 新增 3 篇待读论文/技术报告，暂无 release log 更新 |

### 每周更新内容包括

* 探索使用 turn-level reward function，加强 agentic 模型训练中对长上下文任务及中间推理过程的监督。
* 分析 reasoning 能力从 pretraining 到 post-training 的构建路径，明确不同训练阶段各自承担的功能及其作用机制。
* 梳理 agentic self-improvement 相关研究，分析现有方法的主要技术路线、局限性及潜在优化方向。

---

## 3. 推荐使用方式

### 每周固定流程

每周维护一次，建议流程如下：

1. 在 `weekly-reading/` 中新建本周阅读清单，例如：`2026-W01.md`。
2. 填写本周待阅读论文的题名、来源、DOI/URL、阅读状态和简要备注。
3. 如本周有开源项目、工具、模型或数据集更新，在 `release-logs/` 中记录对应周次的 release log。
4. 在 `updates/` 中新建本周更新摘要，汇总新增阅读材料、阅读重点和 release log 更新情况。
5. 同步更新 `reading-index.md`、必要时更新 `release-index.md`。
6. 在 README 的 `Latest Updates｜本周更新` 中补充本周入口链接。
7. 阅读完成后，再在 `paper-notes/` 中建立单篇论文阅读笔记。


---

## 4. 目录结构

```text
Weekly-Reading-and-Release-Logs/
├── README.md
├── CONTRIBUTING.md
├── reading-index.md
├── release-index.md
├── status-and-naming-rules.md
│
├── updates/
│   ├── README.md
│   ├── template.md
│   └── 2026-W27.md
│
├── weekly-reading/
│   ├── README.md
│   ├── template.md
│   └── 2026-W27.md
│
├── paper-notes/
│   ├── README.md
│   └── template.md
│
├── release-logs/
│   ├── README.md
│   ├── template.md
│   ├── watchlist.md
│   └── 2026-W27.md
│
├── zotero-export/
│   └── README.md
│
├── assets/
│   └── .gitkeep
│
└── .github/
    ├── pull_request_template.md
    └── ISSUE_TEMPLATE/
        ├── weekly-reading-task.md
        ├── paper-note-request.md
        └── release-log-update.md
```

---

## 5. 各目录说明

### `updates/`

用于记录每周总体更新摘要。  
建议按周建立文件，例如：

```text
2026-W27.md
```

每周更新文件主要记录：

- 本周新增阅读清单；
- 本周新增或更新的阅读笔记；
- 本周发生变化的开源项目 release；
- 需要团队关注或讨论的事项。

---

### `weekly-reading/`

用于维护每周待阅读论文列表。  
每周新建一个 Markdown 文件，例如：

```text
2026-W27.md
2026-W28.md
```

每条论文记录应至少包含：

- Title；
- Authors；
- Year；
- Source / Journal / Conference；
- DOI / URL；
- Assigned To；
- Status；
- Notes。

---

### `paper-notes/`

用于存放单篇论文阅读笔记。  
建议每篇论文单独建立一个 Markdown 文件。

论文笔记不需要写成完整综述，但至少应回答：

1. 这篇论文研究什么问题？
2. 使用了什么方法或数据？
3. 主要发现是什么？
4. 对当前团队研究有什么价值？
5. 有哪些局限或不能直接采用的地方？

---

### `release-logs/`

用于记录需要关注的开源项目、工具、模型或数据集的 release logs。

适合记录的内容包括：

- GitHub release；
- 新版本发布；
- API 变更；
- 模型权重更新；
- 数据集更新；
- 重要 bug fix；
- breaking changes；
- 对团队实验、代码或研究流程可能产生影响的变化。

---

### `zotero-export/`

用于存放从 Zotero 导出的文献条目信息，例如 BibTeX、CSV 或 RIS 文件。  
本目录不建议直接存放出版社 PDF，除非团队确认具有合法共享权限。

---

## 6. 状态标签建议

### 阅读状态

- `To read`：待阅读
- `Reading`：阅读中
- `Done`：已完成
- `Discussed`：已在组会讨论
- `Use in review`：可纳入综述或理论框架
- `Exclude`：不纳入核心材料

### Release 关注状态

- `New`：新发现的 release
- `Tracking`：需要继续关注
- `Reviewed`：已查看并记录
- `Important`：对团队研究或实验有明显影响
- `No action`：已查看，但暂不需要处理
- `Deprecated`：不再继续关注

---

## 7. 命名规范

### 每周阅读清单

```text
YYYY-W##.md
```

示例：

```text
2026-W27.md
```

### 每周 release log

```text
YYYY-W##.md
```

示例：

```text
2026-W27.md
```

### 单篇论文笔记

```text
AuthorYear_ShortTitle.md
```

示例：

```text
Ostrom1990_GoverningCommons.md
```

### 每周总体更新

```text
YYYY-W##.md
```

示例：

```text
2026-W27.md
```

---

## 8. 可以放入本仓库的内容

- 每周阅读清单；
- 论文题名、作者、年份、来源、DOI、URL；
- 单篇论文阅读笔记；
- 开源项目 release notes 摘要；
- 工具、模型、数据集的版本更新记录；
- 不含敏感信息的公开资料链接；
- 与团队研究直接相关的简要备注和判断。

---

## 9. 不建议放入本仓库的内容

- 出版社下载的版权 PDF，除非团队确认有合法共享权限；
- 未脱敏的访谈资料、个人信息或内部数据；
- 合同、财务信息、申报书全文等敏感材料；
- 未公开数据集或合作单位内部材料；
- 无法追溯来源的二手资料；
- 与阅读和工具更新无关的零散讨论。

如涉及未发表数据、内部材料或合作项目内容，建议使用 Private Repository，并严格控制成员权限。

---

## 10. 最低维护标准

每条记录至少应满足以下要求：

1. **有日期**：明确记录发生时间或所属周次。
2. **有来源**：论文、工具、项目或 release 必须保留 DOI、URL 或 GitHub 链接。
3. **有责任人**：阅读任务应明确负责人。
4. **有状态**：能判断该条记录是待阅读、阅读中、已完成、需关注还是无需处理。
5. **有简要判断**：不能只复制标题或链接，应留下最基本的价值判断或备注。

---

## 11. 建议配套工具

- **Zotero Group**：管理文献条目、标签和合法 PDF。
- **GitHub Issues**：分配阅读任务、提醒补充笔记、追踪 release 更新。
- **GitHub Pull Requests**：用于审阅重要笔记或结构性修改。
- **Google Drive / OneDrive / 飞书云文档**：存放大文件、原始材料和不适合放入 GitHub 的资料。
