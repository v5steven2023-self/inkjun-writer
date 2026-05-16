# reduce-ai-tone

## 模式

`rewrite`

## 用途

用于测试改稿模式下，模型能否在保留核心判断的前提下，主动消除模板腔、标准答案腔和预制转折。

## 输入

- `input.md`：一段关于 AI 写作同质化的短文草稿
- 必须保留的核心判断：AI 写作的风险之一是表达路径趋同，写作者要对判断和表达负责

## 关注点

- 是否减轻“时代变化”“首先其次最后”“未来已来”这类预制表达
- 是否通过重组句子和段落节奏来降模板感
- 是否避免只做近义词替换
- 是否遵守 `references/rewrite-few-shots.md` 的句法约束

## 通过标准

- 核心判断不能被改掉
- 输出前应包含 `SKILL.md` 要求的自检信息
- 改写后不应明显保留原文中的模板化骨架
- 关键句应有实质性重写，而不是表面替换

## 建议用法

测试时可直接让模型：

`参考 SKILL.md 和 references/rewrite-few-shots.md，把 tests/cases/rewrite/reduce-ai-tone/input.md 改写到 tests/cases/rewrite/reduce-ai-tone/output.md`
