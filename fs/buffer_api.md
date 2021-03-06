<!-- YAML
added: v6.0.0
-->

`fs` 函数支持传递和接收字符串路径与 Buffer 路径。
后者的目的是使其可以在允许非 UTF-8 文件名的文件系统中工作。
对于大多数普通用途，使用 Buffer 路径是不必要的，因为字符串 API 会自动与 UTF-8 相互转换。

**注意**，在某些文件系统（如 NTFS 和 HFS+），文件名总是被编码为 UTF-8。
在这些文件系统中，传入非 UTF-8 编码的 Buffer 到 `fs` 函数将无法像预期那样工作。

