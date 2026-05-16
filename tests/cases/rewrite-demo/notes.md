# rewrite-demo

## 用途

用于测试 `SKILL.md` 的改稿模式。

## 输入

- `input.md`：原始文章草稿

## 输出

- `output.md`：基于当前 skill 规则改写后的版本

## 关注点

- 是否保留原文核心观点
- 是否重写关键段，而不是只做表面同义替换
- 是否遵守 `references/rewrite-few-shots.md` 的句法约束
- 是否减轻模板感和 AI 腔

## 建议用法

测试时可直接让模型：

`参考 SKILL.md 和 references/rewrite-few-shots.md，把 tests/cases/rewrite-demo/input.md 改写到 tests/cases/rewrite-demo/output.md`
