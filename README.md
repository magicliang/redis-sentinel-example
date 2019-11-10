# redis-sentinel-example
Redis 哨兵的实例网络

## 灵感

inspired by [https://github.com/vhf/redis-sentinel-docker-example].

## notes

- 每个哨兵需要单独的配置文件，防止的进程往里面写东西
- 如果在集群里做过 ，各个 sentinel 的 conf 会发生根本性变化，接下来还是按照 redis1 为 master 的模式启动，会立刻触发一次 FO，导致集群再次换 master，这时候如果有数据复制未完成，会丢数据。

## 启动方案

```bash
# TODO：silent化，制作 sop 启动方式，attach 方式和日志切入方式
docker-compose up
```
