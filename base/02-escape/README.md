运行：

```shell
root@localhost ~/w/d/m/b/02-escape (laboratory)# make
current shell user: root
```

结论：

- 使用 `$$USER` 来引用 shell 的 USER 环境变量。单个 `$USER` 在 Makefile 中会被解释为 Makefile 内部变量或函数调用，而我们需要的是传递给 shell，因此使用 `$$`。
- 在 Makefile 中，使用 `$$` 来引用 shell 环境变量属于 转义 机制的一部分。