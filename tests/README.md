# Tests

这里放的是用于手动测试 `SKILL.md` 的样例。

推荐约定：

- 一个测试场景一个目录
- `input.md` 放原始输入
- `output.md` 放期望输出或一次可接受输出
- `notes.md` 放测试目的、关注点、运行方式

当前目录结构：

```text
tests/
└── cases/
    └── rewrite-demo/
        ├── input.md
        ├── notes.md
        └── output.md
```

新增测试时，直接复制一个 case 目录最省事。
