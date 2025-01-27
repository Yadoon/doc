背景:
在较大的事务中数据库链接被回收
数据库配置:
SQLALCHEMY_POOL_SIZE = 5  
SQLALCHEMY_MAX_OVERFLOW = 3  
SQLALCHEMY_POOL_TIMEOUT = 10

触发error

2024-09-27 10:35:14.777 | INFO     | sqlalchemy.engine.base:connect:3268 - Disconnection detected on checkout, invalidating all pooled connections prior to current timestamp (reason: InvalidatePoolError())
2024-09-27 10:35:14.778 | INFO     | sqlalchemy.engine.base:__init__:145 - Invalidate connection <pymysql.connections.Connection object at 0x7f40b22692e8> (reason: InvalidatePoolError:())
2024-09-27 10:35:14.780 | INFO     | sqlalchemy.engine.base:raw_connection:3292 - Connection <pymysql.connections.Connection object at 0x7f40ac52aef0> invalidated due to pool invalidation; recycling

解决方案:
增加连接池回收的时间
SQLALCHEMY_POOL_RECYCLE = 300