```ini
[XDebug]
    zend_extension = "path/to/php_xdebug.so" ;载入Xdebug
    xdebug.profiler_append = 0
    xdebug.profiler_enable = 0  ;配置是否产生cachegrind.out.%t-%s文件,为0时不产生
    xdebug.profiler_enable_trigger = 0
    xdebug.profiler_output_dir = "/tmp/xdebug" ;xdebug 的数据文件目录
    xdebug.profiler_output_name = "cachegrind.out.%t-%s"
    xdebug.auto_trace = On ;开启自动跟踪
    xdebug.show_exception_trace = On ;开启异常跟踪
    xdebug.trace_output_dir = "/tmp/xdebug"  ;xdebug 的数据文件目录
    xdebug.remote_enable = on ;开启远程调试
    xdebug.remote_handler = "dbgp" ;用于zend studio远程调试的应用层通信协议
    xdebug.remote_host = "127.0.0.1" ;允许连接的zend studio的IP地址
    xdebug.remote_port = 9000 ;反向连接zend studio使用的端口
    xdebug.remote_autostart = Off ;开启远程调试自动启动
    xdebug.collect_vars = On ;收集变量
    xdebug.collect_return = On ;收集返回值
    xdebug.collect_params = On ;收集参数
    xdebug.idekey= PHPSTROM
```