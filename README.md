# inkjun-writer

一个面向中文公众号长文写作的 Markdown Skill。

把长文写作拆成清晰流程：先判断该讨论还是该动笔；一旦进入起草或改写，就按固定顺序处理逻辑、信息、语法和 few-shot 约束，尽量把 AI 常见的空话、模板感和语病压下去。

## 当前实际流程

仓库当前以 [`SKILL.md`](./SKILL.md) 为准，核心只有 2 个模式：

- 讨论模式：当信息不足、目标不清，或用户想先把选题、读者、文章目标聊清楚时使用，最终产出提纲
- 起草模式：当用户已经有提纲、素材或原文时使用，覆盖起草、修改、改写、重构

如果用户同时需要“先聊清楚，再写出来”，默认流程是：

`讨论模式 -> 起草模式`

## 起草模式的强制步骤

起草模式不是直接动笔，而是按下面顺序推进：

1. `逻辑重构`
2. `信息扩充`
3. `信息精炼`
4. `语法检查`
5. `读取 few-shots`
6. `起草 / 改写`

其中有几个关键约束：

- 逻辑重构是必做步骤，而且要先给出重构后的大纲，等用户确认后再继续
- 信息不足时要明确标 `待补`，不能编造案例、数据或事实
- 语法检查要求把文本拆成独立句子，逐句检查主语缺失、宾语缺失、主谓搭配不当、动宾搭配不当
- few-shot 规则来自 [`references/rewrite-few-shots.md`](./references/rewrite-few-shots.md)，在起草模式中是最高优先级规则源
- 输出前必须完成 L0/L1/L2 判定和 Gate 1~3 自检；Gate 不通过时，不应输出终稿

## 仓库结构

```text
.
├── README.md
├── SKILL.md
└── references/
    └── rewrite-few-shots.md
```

## 文件说明

- [`SKILL.md`](./SKILL.md)：技能主文件，定义适用边界、模式切换条件、讨论模式产出、起草模式执行顺序和输出前自检
- [`references/rewrite-few-shots.md`](./references/rewrite-few-shots.md)：起草模式专用规则，定义 L0/L1/L2、Gate 1~3，以及具体改写示例

## 怎么使用这个 Skill

作为本地 skill 使用时，入口就是 [`SKILL.md`](./SKILL.md)。

典型调用思路：

1. 先根据用户诉求判断进入讨论模式还是起草模式
2. 如果进入起草模式，必须继续读取 [`references/rewrite-few-shots.md`](./references/rewrite-few-shots.md)
3. 按 `逻辑重构 -> 信息扩充 -> 信息精炼 -> 语法检查 -> few-shots -> 起草/改写` 的顺序执行
4. 输出前补充 L0/L1/Gate 自检，不通过就继续改

## 致谢

这个 Skill 的整理和迭代，受到了下面两个项目的启发。这里单独致谢：

- 卡兹克：https://github.com/KKKKhazix/khazix-skills
- 汤姆喵：https://github.com/tomczhang/tommiao-writer
