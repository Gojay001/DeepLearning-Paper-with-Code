---
name: add-paper-readme
description: Search for deep learning papers and add entries to README.md with Title/Paper/Conf/Code table rows. Use when the user asks to add a paper, update the paper list, append to README tables, or mentions paper names/abbreviations with optional domain or code repo hints.
---

# Add Paper to README

将用户输入的论文（简称或附带领域、代码仓库等线索）检索补全后，写入仓库根目录 `README.md` 对应分类表格。

## 触发场景

- 用户说「添加 XXX 论文」「把 XXX 加到 README」
- 用户提供论文简称（如 `LEDITS++`、`YOLOv8`）或一批论文名
- 用户附带领域、代码仓库、会议等额外信息

## 工作流

```
Task Progress:
- [ ] 1. 解析用户输入
- [ ] 2. 检索论文信息
- [ ] 3. 读取 README.md，确定分类与插入位置
- [ ] 4. 写入表格行
- [ ] 5. 校验信息
- [ ] 6. 询问用户是否提交 git
```

### Step 1: 解析用户输入

从输入中提取：

| 字段 | 说明 |
|------|------|
| **简称** | 表格 `Title` 列，如 `LEDITS++` |
| **全称线索** | 用户若已给出全称，优先采用 |
| **领域/分类线索** | 如「AIGC」「人脸编辑」「检测」 |
| **代码仓库线索** | GitHub URL 或 org/repo 名 |
| **会议线索** | 如 CVPR 2024 |

支持一次处理多篇论文；每篇独立检索、校验、写入。

### Step 2: 检索论文信息

按优先级搜索（至少查 2 个来源交叉验证）：

1. [arXiv](https://arxiv.org/) — **Paper 链接首选**
2. [Semantic Scholar](https://www.semanticscholar.org/)
3. [Google Scholar](https://scholar.google.com.hk/?hl=zh-CN)
4. [Hugging Face Trending Papers](https://huggingface.co/papers/trending)

检索目标：

- **全称**（Paper 列链接文字）
- **arXiv / 官方 PDF 链接**（首选 `https://arxiv.org/abs/...`）
- **会议/期刊 + 年份**（Conf 列）
- **官方代码仓库**（Code 列）

**Conf 格式**（与现有条目一致）：

- 仅有 arXiv：`arXiv(YYYY)`
- 仅有会议/期刊：`CVPR(2024)`
- 两者都有：`arXiv(2023) / CVPR(2024)`（arXiv 在前，空格 + `/` + 空格分隔）

**Code 框架判断**（查看仓库 README、依赖、源码后标注）：

| 框架 | 识别依据 |
|------|----------|
| PyTorch | `import torch`、`requirements.txt` 含 torch、README 写明 PyTorch |
| TensorFlow | `import tensorflow`、TF 模型/checkpoint |
| Caffe | `.prototxt`、Caffe 部署说明 |
| PaddlePaddle | `import paddle` |
| JAX | `import jax` |
| 无法判断 / 无仓库 | 使用 `[code]`；有仓库但框架不明时用 `[GitHub](url)` |

### Step 3: 确定分类并写入 README

1. **读取** `README.md` 全文
2. **对照** [categories.md](categories.md) 中的分类 ↔ 章节映射
3. **默认**：放入已有分类表格；**仅当用户明确要求新建分类**时才新增 `##` / `###` 章节与 TOC 条目
4. **检查重复**：若 `Title` 已存在，告知用户并询问是否更新而非重复添加
5. **插入位置**：同一表格内按字母/时间顺序，或与相邻条目风格保持一致

**表格行格式**：

```markdown
| {Title} | [{Full Title}]({paper_url}) | {Conf} | [{Framework}]({code_url})
```

无代码仓库时：

```markdown
| {Title} | [{Full Title}]({paper_url}) | {Conf} | [code]
```

**字段说明**：

| 列 | 含义 |
|----|------|
| Title | 论文简称 |
| Paper | 全称 + 链接（首选 arXiv） |
| Conf | 会议/期刊；arxiv 与正式发表同时存在则都记 |
| Code | 官方仓库 + 框架标注 |

### Step 4: 校验信息

写入后逐项检查，不确定项**列出并请求用户确认**，不要静默猜测：

| 检查项 | 方法 |
|--------|------|
| 简称 ↔ 全称 | 全称应包含简称或公认别名 |
| Paper 链接 | 访问/抓取确认标题与全称一致 |
| Conf | 交叉对比 Semantic Scholar、论文 PDF、会议 open access |
| Code 仓库 | 确认为论文作者/官方实现；链接可访问 |
| 框架标签 | 与仓库实际技术栈一致 |
| 分类 | 与论文任务/方法匹配 |

校验通过后，向用户展示完整新增行及所属分类，供最终确认。

### Step 5: Git 提交

**信息无误且用户确认后**，主动询问：

> 是否将更改提交到 git？

用户确认后再执行 git 操作。遵循仓库 commit 规范：

1. `git status`、`git diff`、`git log -1` 了解当前状态与 commit 风格
2. 仅 stage 相关文件（通常 `README.md`）
3. Commit message 示例：

```
docs(readme): add LEDITS++ to Face Editing

Add paper entry with arXiv link, venue info, and official PyTorch repo.
```

4. **不要**自动 push，除非用户明确要求
5. **不要**在用户未确认时 commit

## 示例

用户输入:"添加LEDITS++"。搜索论文全称和链接：[LEDITS++: Limitless Image Editing using Text-to-Image Models](https://arxiv.org/abs/2311.16711)。搜索论文会议期刊：arXiv(2023) / CVPR(2024)。搜索论文代码仓库：[PyTorch](https://github.com/ml-research/ledits_pp)。判断该论文属于AIGC-Applications-Face Editing分类下，把信息加入table：| LEDITS++ | [LEDITS++: Limitless Image Editing using Text-to-Image Models](https://arxiv.org/abs/2311.16711) | arXiv(2023) / CVPR(2024) | [PyTorch](https://github.com/ml-research/ledits_pp)。再次检查该条信息是否无误。检查无误后询问用户是否提交到git。

## 附加资源

- 分类与章节映射见 [categories.md](categories.md)
