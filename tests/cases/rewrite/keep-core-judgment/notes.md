# keep-core-judgment

## 模式

`rewrite`

## 用途

用于测试 `SKILL.md` 的改稿模式，重点验证“保留核心判断”的能力。

## 输入

- `input.md`：一篇关于 AI 演化阶段的中文长文草稿
- 必须保留作者的核心判断：AI 演化的关键在于自主权和生产资料控制权的变化

## 关注点

- 是否保留原文核心观点
- 是否重写关键段，而不是只做表面同义替换
- 是否遵守 `references/rewrite-few-shots.md` 的句法约束
- 是否减轻模板感和 AI 腔

## 通过标准

- 原文核心判断不能被改写成别的结论
- 关键段需要重写，不能只替换近义词
- 输出前需要补齐 `SKILL.md` 要求的自检信息
- `references/rewrite-few-shots.md` 中的禁用句法不能明显出现

## 建议用法

测试时可直接让模型：

`参考 SKILL.md 和 references/rewrite-few-shots.md，把 tests/cases/rewrite/keep-core-judgment/input.md 改写到 tests/cases/rewrite/keep-core-judgment/output.md`
