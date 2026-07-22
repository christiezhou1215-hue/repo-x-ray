# Repo X-Ray for Codex

**Understand any codebase in plain language.**

Repo X-Ray is a small Codex plugin that explains what a project, file, function, or code snippet does. It starts with the big picture, follows the important execution flow, and tells you where to begin reading—without drowning you in jargon or repeating every line.

## What it answers

- What is this project or code for?
- What problem does it solve?
- How does it run from input to output?
- Which files, modules, or functions matter most?
- Where should I start reading?
- Which concepts may be confusing to a newcomer?

## Examples

Explain a repository:

```text
Use $repo-x-ray to explain this project in plain language.
```

Explain one file:

```text
Use $repo-x-ray to tell me what this file does and how it fits into the project.
```

Explain a snippet:

```text
Use $repo-x-ray to walk me through how this code works.
```

Repo X-Ray adjusts the depth to the question. A small function gets a short explanation; a repository gets a compact mental model and reading path.

## Install

Download or clone this repository, then add its root directory as a local Codex marketplace:

```bash
codex plugin marketplace add /absolute/path/to/repo-x-ray-open-source
codex plugin add repo-x-ray@repo-x-ray-marketplace
```

Start a new Codex task after installation so the skill is loaded.

## What makes it different

- Leads with meaning instead of syntax
- Explains intent and data flow instead of paraphrasing every line
- Uses file and line evidence when working with repositories
- Separates observed facts from inference
- Avoids unsolicited critique, refactoring, or redesign
- Adapts to the user's experience and language

## 中文简介

Repo X-Ray 是一个把代码解释成人话的 Codex 插件。它可以说明一个项目、文件、函数或代码片段是什么、怎样运行、哪些部分最重要，以及应该从哪里开始阅读。

```text
使用 $repo-x-ray 帮我解释这个项目。
```

## Contributing

Issues and focused pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
