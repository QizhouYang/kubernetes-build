# Etcd性能测试工具
Dockerfile auto build
## 测试步骤
1. 下载镜像  
2. 运行镜像生成容器，将/go/bin/benchmark复制到本地  
3. 按照该方法测试  
例如：./benchmark --endpoints=https://[ip]:2379 --conns=1 --clients=1 --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/healthcheck-client.crt --key=/etc/kubernetes/pki/etcd/healthcheck-client.key put --key-size=8 --sequential-keys --total=10000 --val-size=256  
详见：http://etcd.doczh.cn/documentation/op-guide/performance.html  

