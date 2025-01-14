在 `Makefile` 中，以下是一些特殊的自动化变量，它们在规则中有特定的用途，可以大大简化编写和维护 `Makefile` 的复杂性：

**$@**

表示规则中的目标文件名。例如，在 `target: dependencies` 规则中，`$@`代表`target`。

**$^**

表示所有的依赖文件列表，以空格分隔，并去重（只包含一次每个依赖）。例如，在 `target: dep1 dep2` 规则中，`$^`代表`dep1 dep2`。

**$<**

表示第一个依赖文件的名称。在隐式规则或者模式规则中经常使用，比如在编译命令中取第一个源文件。

**$?**

表示比目标更新的所有依赖文件列表。用来生成仅需要重新编译的文件。

**$%**

当目标是归档成员时，表示归档成员的名字。例如，在处理 `.a` 静态库中的对象文件时使用。

**$+**

类似于 `$^`，但它不会去重，保留所有列出的依赖。这在某些情况下确保所有依赖项被处理多次（如果多次列出）非常有用。

**$***

表示匹配模式的基名前缀，不包括文件扩展名。用于模式规则中。例如，如果规则是 `%.o: %.c`，那么对于 `foo.c`，`$*` 将是 `foo`。

这些自动化变量使得 `Makefile` 更加灵活和强大，因为它们能够动态地处理文件名和依赖关系，从而减少硬编码路径和名称的需要。
