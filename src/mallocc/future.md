# 特性
SQLite内核和它的内存分配子系统提供以下特性：

    （1）对内存分配失败的健壮处理。


    （2）无内存泄漏。应用程序负责销毁已分配的任


    （3）内存使用限制。


    （4）零分配选项。


    （5）应用程序提供内存分配器


    （6）对防止内存分配失败或堆内存出现碎片提供形式化的保证。


    （7）内存使用统计。


    （8）尽量少调用分配器。


    （9）开放式存取。
