# from-outline

## 模式

`draft`

## 用途

用于测试起草模式下，模型能否根据已有提纲写出完整长文，同时保持观点推进和自然节奏。

## 输入

- `input.md`：包含主题、目标读者、结构提纲和写作要求
- 没有现成案例，不能为了充实内容而编造事实

## 关注点

- 是否根据提纲扩成完整文章，而不是简单扩句
- 是否优先推进观点，而不是堆砌华丽表达
- 是否遵守 `references/rewrite-few-shots.md` 的句法约束
- 是否在素材不足处保持克制

## 通过标准

- 输出前应包含 `SKILL.md` 要求的自检信息
- 正文应保留提纲的核心推进线
- 小标题必须有信息量
- 不能编造具体案例、数据或虚构团队实践
- 语言应减少模板化转折和 AI 腔

## 建议用法

测试时可直接让模型：

`参考 SKILL.md 和 references/rewrite-few-shots.md，根据 tests/cases/draft/from-outline/input.md 进入起草模式，并把结果写到 tests/cases/draft/from-outline/output.md`
