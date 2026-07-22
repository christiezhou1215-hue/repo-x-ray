---
name: repo-x-ray
description: Explain a repository, project, source file, function, class, configuration, query, script, or pasted code in clear plain language. Use when the user asks what code is, what it does, how it runs, how its parts connect, where execution starts, which files to read first, or wants help understanding unfamiliar code without unnecessary jargon.
---

# Repo X-Ray

Explain code so the user can form an accurate mental model quickly. Prioritize meaning and execution over syntax commentary.

## Determine the scope

- For a **repository or project**, inspect its manifests, top-level structure, entry points, configuration, and a small number of representative runtime paths.
- For a **file**, read its imports, exports, main definitions, and important callers or callees when available.
- For a **function, class, or code snippet**, explain its inputs, behavior, output, side effects, and role in the surrounding code.

Inspect the actual code before explaining it. Do not infer a whole system from filenames alone.

## Explain in this order

1. **What it is** — Give a one-sentence explanation before details.
2. **What problem it solves** — Describe the practical purpose in the user's language.
3. **How it works** — Walk through the important execution flow from input to output.
4. **Main parts** — Explain only the files, modules, functions, or concepts needed for the mental model.
5. **Where to start** — For repositories, recommend a short reading order. For isolated code, point to the most important line or block.
6. **What may be confusing** — Clarify non-obvious conventions, terminology, state changes, or external dependencies.

Include only sections that help with the current scope. A short snippet usually needs a few paragraphs, not a report.

## Explanation rules

- Lead with the answer, not the inspection process.
- Use plain language and short concrete examples.
- Introduce technical terms only when they improve accuracy, and define them immediately.
- Explain intent and data movement instead of paraphrasing every line.
- Distinguish facts observed in code from reasonable inference.
- Cite local files and tight line locations when explaining a repository or file.
- Use a small Mermaid diagram only when three or more components or steps are materially easier to understand visually.
- Do not critique, refactor, fix, or redesign the code unless the user asks.
- Match depth to the user's apparent experience. When uncertain, explain for an intelligent beginner without being patronizing.

## Default output

Use this lightweight shape when it fits:

```markdown
## 这是什么

一句话说明代码的用途。

## 它怎么运行

从入口到结果解释关键流程。

## 主要部分

解释必要的文件、模块或函数。

## 从哪里开始看

给出最短阅读路径。
```

Answer in the user's language. If they ask only a narrow question, answer it directly instead of forcing the full structure.
