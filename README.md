## 🔧 My Enhancements (基于原项目的二次开发)

- **HTTP Range 支持**：实现 `206 Partial Content`，支持视频流式播放与断点续传。
- **零拷贝优化**：用 `sendfile` 替代 `mmap+writev`，减少系统调用与内存映射开销。
- **内存安全修复**：修复定时器回调空指针，采用 `std::unique_ptr` 管理定时器生命周期，消除内存泄漏。

原项目地址：[qinguoyi/TinyWebServer](https://github.com/qinguoyi/TinyWebServer)
