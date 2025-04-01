项目描述:
本项目是一个基于C++实现的轻量级服务器框架,核心采用协程技术提升服务器性能。通过自主实现协程调度系统,异步IO处理等关键模块,构建了一个高性能,可扩展的服务器基础框架。

内容:
1.基于ucontext_t实现用户态协程,支持创建,切换和销毁,设计了就绪,运行,挂起三种协程状态机,实现非对称协程模型,支持主协程与子协程高效切换;
2.完成线程相关封装,支持互斥锁,读写锁,信号量等多种同步机制,实现日志系统,支持分级日志输出和异步写入;
3.基于时间堆实现了高精度定时器功能,支持定时事件的添加,修改和删除;
4.实现了N-M协程调度器,支持main函数线程参与调度,结合epoll实现了高效事件驱动,支持IO,定时事件的注册和回调;
5.对常见阻塞式系统调用(sleep/socket IO等)进行hook改造,实现同步调用异步化,大幅提升IO密集型任务性能。
