# docker 常用命令

## 基础命令

### 拉取指定镜像

```shell
docker pull id
```



### 打印所有镜像

```shell
docker images
```



### 删除指定镜像

```shell
docker rmi id
```



### 打印所有容器

```shell
docker ps
```



### 删除指定容器

```shell
docker rm -f id
```

### 运行容器

```shell
sudo docker run -i -t --gpus all --name=tj --shm-size 16G -e NVIDIA_DRIVER_CAPABILITIES=compute,utility -e NVIDIA_VISIBLE_DEVICES=all d06a /bin/bash
```

#### 参数解析

```shell
-it /bin/bash     #交互
-gpus all         #使用gpu
-v /home/cyf      # 指定映射目录
--name cyf         # 指定容器名字
```



## 高级命令

### 打印容器和镜像占用空间大小

```shell
sudo docker system df -v
```

### 容器打包为镜像

```shell
docker commit -a 'author' -m 'instruction' test image_test
```

### 导出镜像

```shell
docker save -o test_tar.tar image_test
```

### 导入镜像

```shell
docker load -i test_tar.tar
```


$$

$$
