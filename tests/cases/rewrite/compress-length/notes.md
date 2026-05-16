# compress-length

## 模式

`rewrite`

## 用途

用于测试改稿模式下，模型能否在不丢失核心观点的前提下，压缩冗余表达，提高信息密度。

## 输入

- `input.md`：一段存在重复铺垫和抽象兜圈的文章草稿
- 必须保留的核心判断：压缩篇幅的目标是提纯判断，而不是单纯缩短字数

## 关注点

- 是否删除重复表达和过度铺垫
- 是否保留文章真正要说的结论
- 是否让每段更紧凑，而不是变得生硬
- 是否遵守 `references/rewrite-few-shots.md` 的句法约束

## 通过标准

- 核心判断不能被删掉或改偏
- 输出前应包含 `SKILL.md` 要求的自检信息
- 重复表达应明显减少
- 改后信息密度应高于原稿

## 建议用法

测试时可直接让模型：

`参考 SKILL.md 和 references/rewrite-few-shots.md，把 tests/cases/rewrite/compress-length/input.md 改写到 tests/cases/rewrite/compress-length/output.md`
