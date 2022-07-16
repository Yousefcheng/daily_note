# dbc

## 环境问题

### Aborted (core dumped)

```shell
# 解除内存限制
ulimit -c unlimited

# 对core文件分配1024个字节
ulimit -c 1024
```



### 关于./run_local_carla098.sh跑起来这个问题

#### 首先，需要把游戏环境在2000端口跑起来

```bash
./CarlaUE4.sh -carla-port=2000
```

#### 然后就可以开心的玩耍了

```
./run_local_carla098.sh
```

#### 关于一些小bug

```python
# /data/user21262872/dbc/deep_bisim4control/CARLA_0_9_8/PythonAPI/carla/agents/navigation/carla_env.py
# 249行
# 由于环境加载缓慢 所以要延长加载时间

self.client.set_timeout(20.0)
```

